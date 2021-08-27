---
description: Поставщик взаимосвязей предоставляет механизм для регистрации профилей и связывания их с профилями, реализованными в разных пространствах имен.
ms.assetid: e6aab944-4ed8-4678-ad35-426f7b4f9a35
ms.tgt_platform: multiple
title: Написание поставщика ассоциаций для взаимодействия
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ef4e73c35c942e56b2636b7fced4c7e468e120
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887439"
---
# <a name="writing-an-association-provider-for-interop"></a>Написание поставщика ассоциаций для взаимодействия

Поставщик взаимосвязей предоставляет механизм для регистрации профилей и связывания их с профилями, реализованными в разных пространствах имен.

Поставщики ассоциаций используются для предоставления стандартных профилей, таких как профиль питания. Это достигается путем записи поставщика ассоциаций в корневое пространство имен/Interop, которое предоставляет экземпляры ассоциаций путем реализации класса, производного от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)). &lt; &gt; Для поддержки обхода перекрестного пространства имен поставщик должен быть зарегистрирован как в корневом, так и в пространстве имен.

Windows Инструментарий управления (WMI) загружает поставщик ассоциаций каждый раз, когда запрос ассоциации выполняется в пространстве имен root или Interop.

**Реализация поставщика взаимосвязей для взаимодействия**

1.  Производные классы от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) и создают статический экземпляр этого производного класса в корневом \\ пространстве имен взаимодействия. Как минимум, следующие свойства должны распространяться на допустимые значения:

    -   [**InstanceID**](/previous-versions//ee309375(v=vs.85))
    -   [**регистереднаме**](/previous-versions//ee309375(v=vs.85))
    -   [**RegisteredOrganization**](/previous-versions//ee309375(v=vs.85))
    -   [**регистередверсион**](/previous-versions//ee309375(v=vs.85))

    Хотя [**InstanceId**](/previous-versions//ee309375(v=vs.85)) уникально определяет экземпляр **\_ Регистередпрофиле CIM**, сочетание **регистереднаме**, **RegisteredOrganization** и **регистередверсион** должно однозначно идентифицировать зарегистрированный профиль в области организации. Дополнительные сведения об отдельных свойствах см. в разделе [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)).

    В следующем примере кода описывается синтаксис для наследования класса **процесспрофиле** от [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) и заполнения статического экземпляра.

    ```syntax
    class ProcessProfile : CIM_RegisteredProfile
    {
    };

    instance of ProcessProfile as $PP
    {
         InstanceID = "Process";
         RegisteredName = "Process";
         RegisteredOrganization = "1"; // Set to "Other"
         OtherRegisteredOrganization = "Microsoft";
         RegisteredVersion = "1.0";
    };
    ```

    > [!Note]  
    > для Windows клиентов свойству **RegisteredOrganization** должно быть присвоено значение 1, а свойству **осеррегистередорганизатион** — значение Microsoft.

     

2.  Создайте поставщик, возвращающий экземпляры ассоциаций [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile). Этот процесс состоит из двух шагов.

    1.  Создайте класс, производный от [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в пространствах имен взаимодействия и реализации. Поскольку один и тот же профиль может быть реализован разными поставщиками, имя класса должно быть уникальным. Рекомендуемое соглашение об именовании — " &lt; Организация &gt; \_ &lt; ProductName &gt; \_ &lt; className &gt; \_ &lt; версии &gt; ". Свойство **конформантстандард** или **манажеделемент** должно указывать квалификатор **MSFT \_ targetNamespace** , содержащий пространство имен, к которому принадлежит этот класс.

        В следующем примере кода описывается синтаксис для наследования \_ класса Microsoft Process \_ елементконформстопрофиле \_ v1 от [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в корневом \\ пространстве имен Interop. В этом примере \_ управляемый элемент процесса Win32 ссылается на корневое \\ пространство имен CIMV2 с помощью квалификатора **MSFT \_ targetNamespace** .

        ```syntax
        #pragma namespace("\\\\.\\root\\interop")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             CIM_RegisteredProfile ref ConformantStandard = $PP;
             [MSFT_TargetNamespace("root\\cimv2")]Win32_process ref ManagedElement = null;
        };
        ```

        В следующем примере кода описывается синтаксис для наследования \_ класса Microsoft Process \_ елементконформстопрофиле \_ v1 от [**CIM \_ елементконформстопрофиле**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в корневом \\ пространстве имен CIMV2. В этом примере согласованный стандарт [**CIM \_ регистередпрофиле**](/previous-versions//ee309375(v=vs.85)) ссылается на корневое \\ пространство имен взаимодействия с помощью квалификатора **MSFT \_ targetNamespace** .

        ```syntax
        #pragma namespace("\\\\.\\root\\cimv2")
        [Provider("ProcessAssociation"),Dynamic]
        Class Microsoft_Process_ElementConformsToProfile_v1: CIM_ElementConformsToProfile
        {
             [MSFT_TargetNamespace("root\\interop")] CIM_RegisteredProfile ref ConformantStandard = $PP;
             Win32_process ref ManagedElement = null;
        };
        ```

        Если квалификатор **MSFT \_ targetNamespace** не задан для свойства, ссылающегося на реализованное пространство имен, фильтр **ресулткласс** оператора "соединители" не будет работать. например, если квалификатор **MSFT \_ TargetNamespace** не указан, следующая Windows PowerShell командной строки не будет возвращать объект: **get-wmiobject-query "-соединители {процесспрофиле. InstanceID =" процесс "}, где ресулткласс =" \_ процесс Win32 "**.

        Квалификатор **MSFT \_ targetNamespace** не может указывать на пространство имен на удаленном компьютере. Например, следующее пространство имен не поддерживается: MSFT \_ targetNamespace ( \\ \\ \\ \\ &lt; RemoteMachine &gt; \\ \\ root \\ \\ Interop).

    2.  Напишите поставщик, возвращающий экземпляры созданного производного класса. Дополнительные сведения см. в разделе [написание поставщика экземпляров](writing-an-instance-provider.md). При доступе к экземплярам перекрестного пространства имен может потребоваться доступ к уровням безопасности клиента. Дополнительные сведения см. в разделе [олицетворение клиента](impersonating-a-client.md).

        Поставщик взаимосвязей должен реализовывать методы [**IWbemServices. креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) и [**IWbemServices. жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) . Реализовать метод [**IWbemServices.Exeккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) необязательно. Так как доступ к этому поставщику можно получить как из корневого взаимодействия, так \\ и из \\ &lt; &gt; пространства имен root, в рамках поставщика не должно быть явной зависимости от пространства имен.

3.  Зарегистрируйте поставщика ассоциаций как в корневом \\ взаимодействии, так и в корневых \\ &lt; &gt; пространствах имен. Дополнительные сведения см. в разделе [Регистрация поставщика экземпляров](registering-an-instance-provider.md).

    В следующем примере кода описывается синтаксис для регистрации поставщика ассоциаций в корневом \\ пространстве имен взаимодействия.

    ```syntax
    #pragma namespace("\\\\.\\root\\interop")
    instance of __Win32Provider as $P
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $P;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

    В следующем примере кода описан синтаксис для регистрации поставщика взаимосвязей в корневом \\ пространстве имен CIMV2.

    ```syntax
    #pragma namespace("\\\\.\\root\\cimv2")
    instance of __Win32Provider as $R
    {
        Name    = "ProcessAssociation" ;
        ClsId   = "{DA13393B-A2D5-4BAC-9BD2-30B092E9EBB8}";
    } ;

    instance of __InstanceProviderRegistration
    {
        Provider = $R;
        SupportsPut = false;
        SupportsGet = TRUE;
        SupportsDelete = false;
        SupportsEnumeration = TRUE;
    };
    ```

4.  Поместите схему для [**\_ елементконформстопрофиле CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile) в реализованное пространство имен. для Windows клиентов это файл interop. mof, расположенный в папке% systemroot% \\ system32 \\ wbem.
5.  Реализуйте интерфейс [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для поставщика.

    Инструментарий WMI использует [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) для загрузки и инициализации поставщика. Метод [**IWbemProviderInit.Iniтиализе**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize) должен быть реализован таким образом, который позволяет вызывать его для двух разных пространств имен. Дополнительные сведения см. [в разделе Инициализация поставщика](initializing-a-provider.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**\_ЕЛЕМЕНТКОНФОРМСТОПРОФИЛЕ CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementconformstoprofile)
</dt> <dt>

[**\_РЕГИСТЕРЕДПРОФИЛЕ CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[Написание поставщика экземпляров](writing-an-instance-provider.md)
</dt> <dt>

[Регистрация поставщика экземпляра](registering-an-instance-provider.md)
</dt> </dl>

 

 
