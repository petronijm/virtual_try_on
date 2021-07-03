# virtual_try_on
Генерация изображений DLS

Данная работа предназначена для наложения на фигуру человека одежды(мешей) в видеоизображении с ипользованием FrankMocap, которая позволяет в реальном времени оценивать движения рук и тела человека в 3D на видеозаписи с одного ракурса, Pytorch3D для рендеринга, MultiGarmentNetwork для того, чтобы прогнозировать геометрию одежды, соотносить ее с формой тела и переносить на новые формы тела и позы. Для этого использовался ресурс https://github.com/pbelevich/virtual-try-on. Надо отметить, что при попытке запустить демку с этого ресурса, как раз отражающую заявленную выше тему, оказалось, что она не работает. Анализ кода позволил предположить, что скорее всего устарели библиотеки Pytorch3D, которые грузились от pbelevich (test -z "$(python -c "import pytorch3d" 2>&1)" || pip install -q 'git+https://github.com/pbelevich/pytorch3d.git@stable'). Замена загрузки на стабильную и обновляемую - pip install -q 'git+https://github.com/facebookresearch/pytorch3d.git@stable', решило проблему.

Мною были использованы free video с сайтов - pixabay.com и www.pexels.com HD качестве и 25 кадр/сек.



https://user-images.githubusercontent.com/66363220/124365146-c8d69d00-dc4e-11eb-90e4-39829c45f9fa.mp4



https://user-images.githubusercontent.com/66363220/124365234-50bca700-dc4f-11eb-8a40-ed37c037c7c1.mp4

