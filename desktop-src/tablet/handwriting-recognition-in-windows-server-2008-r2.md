---
description: Windows Server 2008 R2 добавляет поддержку распознавания рукописного текста на стороне сервера в Windows. В этом разделе описывается распознавание рукописного ввода в Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Распознавание рукописного текста в Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "104070819"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Распознавание рукописного текста в Windows Server 2008 R2

Windows Server 2008 R2 поддерживает распознавание рукописного ввода на стороне сервера. Распознавание на стороне сервера позволяет серверу распознать содержимое из перьевого ввода на веб-страницах. Это особенно полезно, когда пользователи в сети будут указывать термины, интерпретируемые с помощью пользовательского словаря. Например, если у вас есть медицинские приложения, которые запрашивают серверную базу данных для имен пациента, эти имена можно добавить в другую базу данных, на которую можно перекрестно ссылаться при выполнении поиска из рукописной формы Silverlight.

## <a name="set-up-your-server-for-server-side-recognition"></a>Настройка сервера для распознавания Server-Side

Чтобы настроить распознавание на стороне сервера, следует выполнить следующие действия.

- Установка службы рукописного ввода
- Установка поддержки веб-сервера (IIS) и сервера приложений
- Включение роли "возможности рабочего стола"
- Запуск службы ввода Tablet PC

### <a name="install-ink-and-handwriting-services"></a>Установка службы рукописного ввода

Чтобы установить службы рукописного ввода и рукописного текста, откройте Диспетчер серверов, щелкнув значок диспетчера серверов в области быстрого запуска. В меню **функции** выберите команду **Добавить компоненты**. Убедитесь, что установлен флажок **службы рукописного ввода** . На следующем рисунке показано диалоговое окно **Выбор компонентов** с выбранным **службы рукописного ввода** .

![Диалоговое окно "Выбор компонентов" с установленным рукописным вводом и службами рукописного ввода](images/setup-server-1-ink-and-handwriting.png)<br/>
*Диалоговое окно "Выбор компонентов" с установленным рукописным вводом и службами рукописного ввода*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Поддержка установки веб-сервера (IIS) и сервера приложений

Откройте диспетчер сервера, как это делалось на первом шаге. Далее необходимо добавить роли "веб-сервер (IIS)" и "сервер приложений". В меню **роли** выберите команду **Добавить роли**. Откроется мастер добавления ролей. Нажмите кнопку **Далее**. Убедитесь, что выбран **сервер приложений** и **веб-сервер (IIS)** . На следующем рисунке показано диалоговое окно **Выбор ролей сервера** с выбранными ролями **веб-сервер (IIS)** и **сервер приложений** .

![Диалоговое окно "Выбор ролей сервера" с выбранными ролями веб-сервера (IIS) и сервера приложений](images/setup-server-2-select-server-roles.png)<br/>
*Диалоговое окно "Выбор ролей сервера" с выбранными ролями веб-сервера (IIS) и сервера приложений*

При выборе **сервера приложений** будет предложено установить платформу ASP.NET. Нажмите кнопку **Добавить необходимые компоненты** . После нажатия кнопки " **Далее**" отобразится диалоговое окно "Обзор". Нажмите кнопку **Далее**. Теперь должно быть доступно диалоговое окно **Выбор служб ролей** . Убедитесь, что выбран **веб-сервер (IIS)** . На следующем рисунке показано диалоговое окно **Выбор служб ролей** с включенным веб-сервером (IIS).

![Диалоговое окно "Выбор служб ролей" с включенным веб-сервером (IIS)](images/setup-server-3-select-role-services.png)<br/>
*Диалоговое окно "Выбор служб ролей" с включенным веб-сервером (IIS)*

Нажмите кнопку **Далее**. Откроется диалоговое окно обзора. еще раз нажмите кнопку **Далее** . Теперь отобразится страница с предложением параметров для ролей веб-сервера (IIS). Нажмите кнопку **Далее**. На следующей странице кнопка " **установить** " станет активной. Нажмите кнопку **установить** , после чего будет установлена поддержка веб-сервера (IIS) и сервера приложений.

### <a name="enable-the-desktop-experience-role"></a>Включение роли "возможности рабочего стола"

Чтобы включить возможности рабочего стола, нажмите кнопку **Пуск**, выберите пункт **Администрирование**, а затем щелкните **Диспетчер сервера**. Выберите **Добавить службы** , а затем выберите службу " **возможности рабочего стола** ". На следующем рисунке показано диалоговое окно **Выбор компонентов** с установленным элементом "возможности рабочего стола".

![Диалоговое окно "Выбор компонентов" с выбранной службой "возможности рабочего стола"](images/setup-server-4-desktop-experience.png)<br/>
*Диалоговое окно "Выбор компонентов" с выбранной службой "возможности рабочего стола"*

Нажмите кнопку **Далее** , чтобы установить возможности рабочего стола.

### <a name="start-the-tablet-service"></a>Запуск службы планшета

После установки службы "возможности рабочего стола" в меню " **службы** " появится служба ввода Tablet PC. Чтобы открыть меню " **службы** ", нажмите кнопку " **Пуск**", выберите " **Администрирование**", а затем " **службы**". Чтобы запустить службу, щелкните правой кнопкой мыши элемент **служба ввода Tablet PC** и выберите команду **запустить**. На следующем рисунке показано меню **службы** с запущенной службой ввода Tablet PC.

![Меню "службы" с запущенной службой ввода Tablet PC](images/setup-server-5-tablet-pc-input-service.png)<br/>
*Меню "службы" с запущенной службой ввода Tablet PC*

## <a name="performing-server-side-recognition-using-silverlight"></a>Выполнение Server-Sideного распознавания с помощью Silverlight

В этом разделе показано, как создать веб-приложение, которое использует Silverlight для записи рукописного ввода. Чтобы запрограммировать распознаватель в Visual Studio 2008, выполните следующие действия.

- Установите и обновите Visual Studio 2008, чтобы добавить поддержку Silverlight.
- Создайте новый проект Silverlight в Visual Studio 2008.
- Добавьте необходимые ссылки на службы в проект.
- Создание службы WCF Silverlight для распознавания рукописного ввода.
- Добавьте ссылку на службу в клиентский проект.
- Добавьте класс InkCollector в проект Инкрекогнитион.
- Удалите защищенные директивы транспорта из конфигурации клиента.

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>Установка и обновление Visual Studio 2008 для добавления поддержки Silverlight

Перед началом работы необходимо выполнить следующие действия на сервере Windows Server 2008 R2.

- Установите Visual Studio 2008.
- Установите [Microsoft Visual Studio 2008 с пакетом обновления 1 (SP1)](https://www.microsoft.com/download/details.aspx?id=10986).
- Установите [пакет SDK для Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).

После установки этих приложений и обновлений можно приступать к созданию веб-приложения для распознавания на стороне сервера.

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>Создание нового веб-проекта Silverlight в Visual Studio 2008

В меню **Файл** выберите **Новый проект**. Выберите шаблон приложения Silverlight из списка проектов Visual C \# . Присвойте проекту имя Инкрекогнитион и нажмите кнопку **ОК**. На следующем рисунке показан проект C \# Silverlight, выбранный с именем инкрекогнитион.

![\#выбранный проект c Silverlight с именем инкрекогнитион](images/project-1-new-project.png)<br/>
*\#выбранный проект c Silverlight с именем инкрекогнитион*

После нажатия кнопки **ОК** появится диалоговое окно, предлагающее добавить в проект приложение Silverlight. Выберите **Добавить новый веб-проект ASP.NET в решение для размещения Silverlight** и нажмите кнопку **ОК**. На следующем рисунке показано, как настроить пример проекта перед нажатием кнопки **ОК**.

![Диалоговое окно с запросом на Добавление приложения Silverlight в проект](images/project-2-add-a-new-aspnetproject.png)<br/>
*Диалоговое окно с запросом на Добавление приложения Silverlight в проект*

### <a name="add-the-necessary-service-references-to-your-project"></a>Добавление необходимых ссылок на службы в проект

Теперь у вас есть универсальный клиентский проект Silverlight (Инкрекогнитион) с веб-проектом (Инкрекогнитион. Web), настроенным в решении. Проект откроется с помощью Page. XAML и Open. aspx по умолчанию. Закройте эти окна и добавьте ссылки System. Runtime. Serialization и System. ServiceModel в проект Инкрекогнитион, щелкнув правой кнопкой мыши папку References в проекте Инкрекогнитион и выбрав пункт **Добавить ссылку**. На следующем рисунке показано диалоговое окно с выбранными ссылками на реквизиты.

![Диалоговое окно «Добавление ссылок» с выбранным System. Runtime. Serialization и System. ServiceModel](images/project-3a-add-references-to-inkreco.png)<br/>
*Диалоговое окно «Добавление ссылок» с выбранным System. Runtime. Serialization и System. ServiceModel*

Далее необходимо добавить ссылки System. ServiceModel и Microsoft. Ink в проект Инкрекогнитион. Web. Ссылка Microsoft. Ink не будет отображаться в ссылках на .NET по умолчанию, поэтому выполните поиск Microsoft.Ink.dll в папке Windows. После того как библиотека DLL будет найдена, добавьте сборку в ссылки проекта: выберите вкладку **Обзор** , перейдите в папку, содержащую Microsoft.Ink.dll, выберите Microsoft.Ink.dll и нажмите кнопку **ОК**. На следующем рисунке показано решение проекта в проводнике Windows со всеми добавленными эталонными сборками.

![проект инкрекогнитион в проводнике Windows со всеми добавленными эталонными сборками](images/project-3b-with-reference-assemblies.png)<br/>
*проект инкрекогнитион в проводнике Windows со всеми добавленными эталонными сборками*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>Создание службы WCF Silverlight для распознавания рукописного ввода

Далее предстоит добавить службу WCF для распознавания рукописного текста в проект. Щелкните правой кнопкой мыши проект Инкрекогнитион. Web, выберите **Добавить**, а затем — **новый элемент**. Выберите шаблон службы WCF Silverlight, измените имя на Инкрекогитионсервице и нажмите кнопку **Добавить**. На следующем рисунке показано диалоговое окно **Добавление нового элемента** со службой WCF Silverlight и именем.

![Диалоговое окно "Добавление нового элемента" с выбранной и именованной службой WCF Silverlight](images/project-4-add-wcf-service.png)<br/>
*Диалоговое окно "Добавление нового элемента&quot; с выбранной и именованной службой WCF Silverlight*

После добавления службы WCF Silverlight будет открыт код службы, Инкрекогнитионсервице. cs. Замените код службы следующим кодом.

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = &quot;")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a>Добавление ссылки на службу в клиентский проект

Теперь, когда у вас есть служба Silverlight WCF для Инкрекогнитион, вы будете использовать службу из клиентского приложения. Щелкните правой кнопкой мыши проект Инкрекогнитион и выберите **Добавление ссылки на службу**. В появившемся диалоговом окне **Добавление ссылки на службу** выберите **обнаружить** , чтобы найти службы из текущего решения. Инкрекогнитионсервице появится в области службы. Дважды щелкните Инкрекогнитионсервице в области службы, измените пространство имен на Инкрекогнитионсервицереференце и нажмите кнопку **ОК**. На следующем рисунке показано диалоговое окно **Добавление ссылки на службу** с выбранным инкрекогнитионсервице и измененным пространством имен.

![Диалоговое окно "Добавление ссылки на службу" с выбранным инкрекогнитионсервице и измененным пространством имен](images/project-5-discover-service-reference.png)<br/>
*Диалоговое окно "Добавление ссылки на службу" с выбранным инкрекогнитионсервице и измененным пространством имен*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>Добавление класса InkCollector в проект Инкрекогнитион

Щелкните правой кнопкой мыши проект Инкрекогнитион, выберите **Добавить**, а затем щелкните **новый элемент**. В меню **Visual C \#** выберите **\# класс c**. Присвойте классу имя InkCollector. На следующем рисунке показано диалоговое окно с \# выбранным классом C и именем.

![Диалоговое окно "Добавление нового элемента" с \# выбранным классом c и именем](images/project-6-add-ink-collector.png)<br/>
*Диалоговое окно "Добавление нового элемента" с \# выбранным классом c и именем*

После добавления класса InkCollector будет открыто определение класса. Замените код в сборщике рукописного ввода на следующий код.

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a>Обновление XAML для страницы по умолчанию и добавление кода программной части для распознавания рукописного текста

Теперь, когда у вас есть класс, собирающий рукописный ввод, необходимо обновить XAML в Page. XAML, используя следующий код XAML. Следующий код добавляет желтый градиент к области ввода, элементу управления InkCanvas и кнопку, запускающую распознавание.

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

Замените страницу кода программной части Page. XAML. cs следующим кодом, который добавит обработчик событий для кнопки **распознать** .

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>Удалите защищенные директивы транспорта из конфигурации клиента.

Прежде чем можно будет использовать службу WCF, необходимо удалить все параметры безопасного транспорта из конфигурации службы, так как в настоящее время защищенные транспортные протоколы не поддерживаются в службах WCF Silverlight 2,0. В проекте Инкрекогнитион обновите параметры безопасности в Сервицереференцес. Клиентконфиг. Изменение XML-кода безопасности с

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

значение

```XML
       <security mode="None"/>
```

Теперь приложение должно работать. На следующем рисунке показано, как приложение выглядит в пределах авебпажевис рукописного ввода, указанного в поле распознавания.

![Приложение в авебпажевис. Некоторые рукописные данные, указанные в поле распознавания](images/demo-1.png)<br/>
*Приложение в авебпажевис. Некоторые рукописные данные, указанные в поле распознавания*

На следующем рисунке показан распознанный текст в раскрывающемся списке **результатов** .

![Приложение внутри авебпажевис распознанного текста в раскрывающемся списке результатов](images/demo-2.png)<br/>
*Приложение внутри авебпажевис распознанного текста в раскрывающемся списке результатов*

 

 



