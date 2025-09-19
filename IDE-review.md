# Обзор IDE

<div align="center">
 
![logo](https://user-images.githubusercontent.com/28728575/124395667-9f2c7d00-dd05-11eb-8fa3-9780a7132e96.png) 
*Среды, поддерживающие Python*

</div>

Здесь представлено краткое описание тех или иных программных средств (далее IDE), которые будут использоваться в течение всего курса для написания кода на языке Python. Информация, которую вы можете найти здесь:
- описание
- установка
- основной функционал

## 📋 Содержание
1. [Быстрое начало](#start)
2. [Google Colaboratory](#colab)
   1. [Функционал](#colab_features)
4. [Python](#python) 
   1. [Установка](#python_install)
   2. [IDLE](#IDLE)
   3. [PIP](#pip)
3. [Jupyter](#jupyter)
   1. [Установка](#jupyter_setup)
   2. [Функционал](#jupyter_features)
   3. [Установка с помощью Miniconda](#miniconda)


## ⏳ Быстрое начало  <a name="start"></a>
Данный пункт - это краткий справочник для запуска вашего первого кода.
Более подробная информация представлена в следующих разделах. 

### Инструкция
1. Перейдите в [Google Drive](https://drive.google.com/drive/);
2. Создайте и перейдите в `Google Colaboratory`; 
   >Если пункт не отображается, нажмите на `Подключить другие приложения`
3. Напишите в  ячейке:
   ```python
   print('Hello World!')
   ```
   И нажмите <kbd>SHIFT</kbd>+<kbd>ENTER</kbd> для запуска.

Должно выглядеть следующим образом:

<!---
How to find textwidth of line?
-->
<div align="center">
<img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/124350962-f6442c00-dbf7-11eb-8cb3-36489c235f56.png">
<img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/124350977-fe9c6700-dbf7-11eb-9ffd-e66761f6d2e5.png">
</div>

[comment]: <> (Solarized dark             |  Solarized Ocean)
[comment]: <> (:-------------------------:|:-------------------------:)
[comment]: <> (![im1][1] |  ![im2][2])

Теперь вы можете начать писать собственный код без установки
дополнительных приложений/программ и т.д. Все, что вам требуется — подключение к интернету 
и Google аккаунт.

## Google Colaboratory  <a name="colab"></a>

Google Colaboratory (либо просто *Colab*) — это бесплатный __облачный__ сервис,
который позволяет писать и выполнять код Python прямо в браузере. 
Как утверждает Google, это отличное решение, которое:
- не требует никакой настройки;
- выполняет (компилирует) код на серверах с большой вычислительной мощностью;
- при желании дает доступ для совместного пользования с другими людьми.

Colab основан на *Jupyter Notebook* (о нем поговорим позже) и предоставляет все
необходимое для студентов, специалистов по обработке данных и 
исследователей в области искусственного интеллекта. Также можете посмотреть полезное ознакомительное видео по [ссылке][3]. 

<img width="1408" alt="Google colab" src="https://user-images.githubusercontent.com/28728575/124363089-7b036a00-dc39-11eb-86d7-ca11383cfa7d.png">

### Возможности Colab <a name="colab_features"></a>

Предполагается, что вы уже освоили [Быстрое начало](#start).


Вы можете редактировать ваш блокнот совместно с другими пользователями, оставлять комментарии, предоставлять различные права доступа к документу, то есть работать точно также как и с любым документом на Google Drive. Но, помимо этого, есть некоторые особенности, которые лучше освоить перед началом работы.

1. __Копирование на свой диск__
   
   Чужие блокноты (у которых открыт доступ) можно добавлять на свой Диск:
   - Откройте [какой-нибудь][4] блокнот;
   - Нажмите на `Копировать на Диск` или перейдите в `Файл` и нажмите 
     `Сохранить копию на диске`;
     > На диске создастся папка под названием Colab Notebooks, в которой
     > будут храниться все добавленные проекты.
     <img width="400" alt="copy on disk" src="https://user-images.githubusercontent.com/28728575/124400230-3bb04880-dd21-11eb-9cc7-2883b8d511d7.png">


2. __Выполнение всех ячеек__
   - Перейдите `Среда выполнения`
     и нажмите `Выполнить все`;
     
   или  
   - Зажмите <kbd>CTRL</kbd>+<kbd>F9</kbd> (или <kbd>⌘</kbd>+<kbd>F9</kbd> 
     на Mac).
     
     <img width="400" alt="run all" src="https://user-images.githubusercontent.com/28728575/124400320-ce50e780-dd21-11eb-839d-7e93f5a63226.png">



3. __Аппаратный ускоритель__
   
   Есть возможность ускорять сложные вычислительные задачи за счет облачных серверов:
   - Перейдите `Изменить → Настройки блокнота`;
   - В окне `Аппаратный ускоритель` выберите `GPU` или `TPU` и нажмите `Сохранить`.
      > На самом деле GPU и TPU являются одной и той же технологией. Единственное
      > отличие в том, что TPU (*Tensor Processing Units*) — собственное оборудование от Google
      > специально разработанное для машинного обучения.
   
   <img width="400" alt="accelerates 1" src="https://user-images.githubusercontent.com/28728575/124400359-18d26400-dd22-11eb-8cc9-d066b8fad6d4.png">
   <img width="400" alt=accelerates 2" src="https://user-images.githubusercontent.com/28728575/124400371-330c4200-dd22-11eb-98bd-780ff373bde2.png">
    
   Для обычных задач (с которыми мы будем работать в наших курсах) смысла в использовании этой технологии нет. Этот раздел пригодится вам в следующих курсах. 
     
  
4. __Ячейки можно использовать не только для кода__
    
    Основное отличие Colab от Jupyter заключается в том, что тут
    можно запускать базовые _консольные_ команды.
    
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/124385674-0da61680-dcd7-11eb-8141-e53e952f1bc3.png">

5. __Скачивание блокнотов__

    - Перейдите `Файл→Скачать` и нажмите на `Скачать IPYNB`.
    
     <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125208846-a91e2500-e29d-11eb-8449-df335ce31cd3.png">

6. __Взаимодействие с Git__

    Блокнот Colab может быть загружен из репозитория __GitHub__:
    > Если у вас нет опыта работы с _git_, рекомендуем пропустить этот пункт.
    - Откройте пустой блокнот и перейдите по `Файл → Открыть блокнот` или
    зажмите <kbd>CTRL</kbd>+<kbd>O</kbd> (<kbd>⌘</kbd>+<kbd>O</kbd>);
    - В появившемся окне выберите **`GitHub`** и введите ссылку на
    блокнот в репозитории, например, [эту][5] и нажмите на поиск.
    
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/124400473-f4c35280-dd22-11eb-9ab4-b77560f33a5c.png">
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/124400455-d2c9d000-dd22-11eb-88ea-a71e67505836.png">


   
    Также вы можете сохранить свой блокнот в репозитории:
    - Перейдите по `Файл → Создать копию в GitHub`.
        > В первый раз потребуется авторизация в аккаунт.
    
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/124400503-348a3a00-dd23-11eb-8729-15dc8f87ce47.png">
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/124400513-4c61be00-dd23-11eb-89fb-ceab4cae9674.png">

## Python <a name="python"></a>

Перед тем, как переходить к следующим пунктам, необходимо установить [интерпретатор Python](https://www.python.org/about/).

### Установка <a name="python_install"></a>

Перейдите по [ссылке][7] и нажмите соответствующую кнопку для скачивания. Далее необходимо пройти
самую обычную процедуру установки.
 
<div align="center">
<img height="250" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125459310-cbc043d1-a3a2-44c3-8d84-8389d407e48c.png">

<img height="250" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/125459421-fe83516e-b459-49ef-94f5-b8bf59cfa643.png">
</div>
 
Для корректной работы на **Windows** перед установкой `Install Now` необходимо нажать на `Add Python to PATH`.
 
<div align="center">
<img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/127037734-7f0d2ec3-9fe3-46c7-8ea6-c26f78188069.png">
</div>




Чтобы убедиться, что все установлено корректно:
- На __Mac (Linux)__ откройте терминал и введите:
    ```shell
    python3
    ```
- После чего напишите:
    ```python
    print("Hello World!")
    ```
    и нажмите <kbd>ENTER</kbd> для запуска. 

    Должно выглядеть следующим образом:
    
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125427198-4696ecd2-1b57-4be4-95a9-de45a5887745.png">


- На __Windows__ откройте командую строку и введите:
    ```shell
    python
    ```
    или
    ```shell
    py
    ```
    
    
- После чего напишите:
    ```python
    print("Hello World!")
    ```
    и нажмите <kbd>ENTER</kbd> для запуска.

    Должно выглядеть следующим образом:
    
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/126388309-068f2167-6ba2-4cde-8872-ec87704dfe61.png">


Теперь вы знаете, как _быстро_ написать пару строчек кода в среде терминала (командной строки).
>На самом деле писать здесь полноценный код для проекта не рекомендуется (да и не получится) в силу 
>неудобства, так как вычисления проводятся после каждой написанной строчки. 
 
### IDLE <a name="IDLE"></a>

После установки _Python_ у вас должно появиться **IDLE** (_Integrated DeveLopment Environment_) — упрощенный редактор, который отлично подходит для начала программирования
и понимания основ языка. Несмотря на простоту, он включает в себя автозавершение кода, подсветку синтаксиса, 
подбор отступа и т.п.

<img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125690969-4ea4bc98-95ed-4bd2-8c1d-a3c51a0c4203.png">

Процесс написания кода здесь такой же, как и в терминале (командной строке), т.е. компилирование происходит после каждой строчки,
что является неудобным. Поэтому обычно создают отдельные файлы:
- Перейдите по `File→New File` или нажмите на <kbd>CTRL</kbd>+<kbd>N</kbd> (<kbd>⌘</kbd>+<kbd>N</kbd>);
- Напишите какой-нибудь код, например:
    ```python
    age = 20
    print("Мне %d лет!" %age)
    ```
- Запустите файл (но перед этим сохраните) с помощью `Run→Run Module` или <kbd>F5</kbd>.
     <img width="500" alt="Untitled-1" src="https://user-images.githubusercontent.com/28728575/125693688-9bff9e50-ef2b-4fa8-8673-0f5e9891b270.png">
 
### PIP <a name="pip"></a>

Для полноценной работы с языком _Python_ вам необходимы библиотеки (далее пакеты), которые могут упростить написание 
вашего проекта. Например, в пакете _numpy_ реализованы многочисленные методы взаимодействия с числами.
Для установки таких пакетов пользуются специальным инструментом **PIP** 
(_Pip Installs Packages_ — рекурсивный акроним).
> Если установка Python была произведена со стандартными настройками, то PIP уже находится на вашем
> устройстве.

Перед началом работы __обновите__ версию PIP до последней с помощью следующей команды в терминале (командной строке):

- **Mac (Linux)**
    ```shell
    pip install -U pip
    ```
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125447876-1ba39969-3ff3-40c8-9b68-635841c9d7c4.png">
 
 > Так же _обратите внимание_, что у некоторых пользователей Mac могут возникнуть ошибки для команд, которые начинаются с `pip`. В этом случае просто замените `pip` на `pip3`. **Пример**:  `pip install -U pip` → `pip3 install -U pip`
- **Windows**
    ```shell
    pip install --upgrade pip
    ```
    или
    ```shell
    pip install --upgrade pip
    ```

    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/127038235-407c7c3e-a7aa-47a2-ac99-4e1053e1e740.png">

  
#### Основные команды
Полный набор команд можно посмотреть в [официальной документации][8].
- Установка пакетов:
    ```shell
    pip install package-name
    ```
- Установка определенной версии:
    ```shell
    pip install package-name==1.0.0
    ```
- Доступные версии пакета:
    ```shell
    pip install package-name==
    ```
- Основная информация про пакет:
    ```shell
    pip show package-name
    ```
- Список всех устаревших пакетов:
    ```shell
    pip list --outdated
    ```
- Обновление устаревшего пакета:
    ```shell
    pip install package-name --upgrade
    ```
- Принудительно установить (переустановить) определенную версию пакета:
    ```shell
    pip install --upgrade --force-reinstall package-name==1.0.0
    ```
- Удалить пакет:
    ```shell
    pip uninstall package-name
    ```


## JupyterLab <a name="jupyter"></a>
[JupyterLab][6] — это интерактивная среда разработки и работы с **блокнотами**, кодом и данными.
Крайне удобный инструмент не просто для программирования, а также для создания красивых
визуальных проектов с графиками, изображениями, комментариями и т. д. 
Поэтому данная среда получила широкое распространение в области науки о данных, 
научных вычислениях и машинном обучении.

Данный пункт можно расценивать как некое дополнение к [Google Colab](#colab),
так как он был разработан на основе Jupyter.
> Существует также Jupyter Notebook, который со временем эволюционировал в
> JupyterLab. Рассматривать его отдельно мы не будем, так как он имеет меньший функционал.

![jupyter_image](https://jupyter.org/assets/labpreview.png)

**ВНИМАНИЕ**: <a name="jupyter_setup"></a> \
Следующая установка предполагает использование специального инструмента [PIP](#pip), про который мы писали выше. К сожалению, у некоторых пользователей могут возникнуть проблемы. Поэтому мы __рекомендуем__ пройти установку c помощью [Miniconda](#miniconda). Это распространный дистрибутив, который создает единую надежную среду, где будут храниться _Python_, _conda_ (аналог _PIP_) и библиотеки. Подробнее можно прочитать [здесь][9].

### Установка

Единственное, что вам потребуется — установленный [Python](#python).

- Введите в терминале/командой строке следующее:
    ```shell
    pip install jupyterlab
    ```
- Дождитесь окончания загрузки и запустите с помощью:
    ```
   jupyter-lab
   ```
   
После этого в браузере должно открыться соответствующее окно:

<img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125204616-c8f61e80-e286-11eb-9bb0-0463c9e7f09d.png">

### Как пользоваться JupyterLab <a name="jupyter_features"></a>
Если вы уже освоились в Colab, то все должно быть интуитивно понятно.

1. __Блокнот__
    
    В режиме _Notebook_ все свойства аналогичны свойствам Google Colab.  
    - Cкачайте блокнот по [ссылке][5];
    - Откройте ваш блокнот в директории: 
      
      <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125456239-f59b38b8-ccf4-4b13-b6de-41e2b14929e4.png">
    - Запустите все ячейки:
    
        <img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/125457661-c0f4ded8-e204-4b31-ab41-b83b624b9ed9.png">
   
    Также вы можете создать свой собственный блокнот.
    - Нажмите на `+` и выберите соответствующую иконку под `Notebook`:
    
    <div align="center">
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/125457018-68eb7ccd-888d-4bb0-9beb-a076d5397dc8.png">
    <img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/125457235-74d1706f-44e3-4e43-ba45-3d6c45a8d677.png">
    </div>

2. __Console/Terminal__ 
    
    Режим __Console__ вы можете использовать как единичную ячейку в блокноте. Часто это бывает удобно,
    чтобы скачать какой-нибудь пакет, проверить работоспособность строчки кода и т. д.
    
    <img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/125458782-a3f8fd9c-5671-4cfc-ade2-b46e7f8de5d3.png">
   
    Режим __Terminal__ аналогичен терминалу (командной строке).

    <img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/125458912-30858cd9-22c8-48ab-a665-10137593f726.png">


### Miniconda <a name="miniconda"></a>
 
1. __Установка Miniconda__
 
   Для начала нужно установить Miniconda по следующей [ссылке](https://docs.conda.io/en/latest/miniconda.html). И Windows, и MacOS имеют графические установщики (файл .pkg для MacOS). Пройдите самую обычную установку, не нажимая дополнительных галочек. 
  
  <div align="center">
    <img width="400" alt="Screenshot 2021-07-03 at 12 09 57" src="https://user-images.githubusercontent.com/28728575/136696592-b3cc4a50-9416-4542-9087-04a07fc3ec88.png">
    <img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/136696602-75adfc85-aeda-4e6c-96c7-3b86baa7a021.png">
 
 *Скриншоты для установки на Windows. Аналогично для других систем*
    </div>
 
 2. __Проверьте, что установка прошла успешно__
    
    - Пользователи Windows всегда должны начинать с запуска программы **Anaconda Prompt**.
    
      <img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/136696892-7a98f938-e616-43b6-9133-13d1a0832ae4.jpg">
 
      Пользователи MacOS/Linux, запустите терминал.
 
     - Введите `conda list`. Если установка прошла успешно, должно высветиться что-то подобное (содержание Miniconda):

       <img width="400" alt="Screenshot 2021-07-03 at 12 12 16" src="https://user-images.githubusercontent.com/28728575/136697005-630e667d-e5d3-4ccf-8754-6bc78998aa99.png">


  3. __Установка JupyterLab__
 
     - Введите, чтобы началась загрузка:
 
       ```bash
       conda install -c conda-forge jupyterlab
       ```
 
     - Для запуска введите `jupyter lab` для пользователей Windows, `jupyter-lab` для пользователей MacOS/Linux.

 

[1]: https://user-images.githubusercontent.com/28728575/124350962-f6442c00-dbf7-11eb-8cb3-36489c235f56.png
[2]: https://user-images.githubusercontent.com/28728575/124350977-fe9c6700-dbf7-11eb-9ffd-e66761f6d2e5.png
[3]: https://www.youtube.com/watch?v=inN8seMm7UI
[4]: https://colab.research.google.com/drive/1gtz6e4zcCqK4bSSeuiX12q5bomtO7q1n?authuser=1
[5]: https://github.com/MSUcourses/IDE-review/blob/main/%D0%9F%D0%B5%D1%80%D0%B2%D0%BE%D0%B5_%D0%B7%D0%BD%D0%B0%D0%BA%D0%BE%D0%BC%D1%81%D1%82%D0%B2%D0%BE.ipynb
[6]: https://jupyter.org/ 
[7]: https://www.python.org/downloads/
[8]: https://pip.pypa.io/en/stable/cli/
[9]: https://medium.com/dunder-data/anaconda-is-bloated-set-up-a-lean-robust-data-science-environment-with-miniconda-and-conda-forge-b48e1ac11646

