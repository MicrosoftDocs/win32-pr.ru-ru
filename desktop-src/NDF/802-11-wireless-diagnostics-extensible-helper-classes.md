---
title: Расширяемые вспомогательные классы диагностики беспроводной сети 802,11
description: Встроенная инфраструктура диагностики беспроводной связи имеет две точки расширения. Родительский вспомогательный метод Класспурпосеревисед Native WiFi (РНВФ) расширяемый вспомогательный метод Классдиагносес проблемы, связанные с расширениями подключения 802,11.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde49561c68044157c9d518571b8241c49dcf25
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104533017"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a><span data-ttu-id="a5c63-103">Расширяемые вспомогательные классы диагностики беспроводной сети 802,11</span><span class="sxs-lookup"><span data-stu-id="a5c63-103">802.11 Wireless Diagnostics Extensible Helper Classes</span></span>

<span data-ttu-id="a5c63-104">Встроенная инфраструктура диагностики беспроводной связи имеет две точки расширения.</span><span class="sxs-lookup"><span data-stu-id="a5c63-104">The built-in wireless diagnostics infrastructure has two extension points.</span></span>

| <span data-ttu-id="a5c63-105">Родительский вспомогательный класс</span><span class="sxs-lookup"><span data-stu-id="a5c63-105">Parent Helper Class</span></span>                                | <span data-ttu-id="a5c63-106">Назначение</span><span class="sxs-lookup"><span data-stu-id="a5c63-106">Purpose</span></span>                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="a5c63-107">Пересмотрен собственный расширяемый вспомогательный класс WiFi (РНВФ)</span><span class="sxs-lookup"><span data-stu-id="a5c63-107">Revised Native Wifi (RNWF) Extensible Helper Class</span></span> | <span data-ttu-id="a5c63-108">Диагностика проблем, связанных с расширениями подключения 802,11.</span><span class="sxs-lookup"><span data-stu-id="a5c63-108">Diagnoses issues related to 802.11 connectivity extensions.</span></span>       |
| <span data-ttu-id="a5c63-109">Расширяемый вспомогательный класс L2Security</span><span class="sxs-lookup"><span data-stu-id="a5c63-109">L2Security Extensible Helper Class</span></span>                 | <span data-ttu-id="a5c63-110">Диагностика проблем, связанных с расширениями протокола безопасности уровня 2.</span><span class="sxs-lookup"><span data-stu-id="a5c63-110">Diagnoses issues related to Layer 2 security protocol extensions.</span></span> |



 

> [!Note]  
> <span data-ttu-id="a5c63-111">Сторонний вспомогательный класс должен зарегистрироваться в обоих родительских вспомогательных классах, чтобы гарантировать вызов стороннего класса.</span><span class="sxs-lookup"><span data-stu-id="a5c63-111">A third-party helper class should register with both parent helper classes to ensure that the third-party class gets called.</span></span> <span data-ttu-id="a5c63-112">Дополнительные сведения о регистрации см. в разделе [Регистрация расширений вспомогательного класса ndf](registering-ndf-helper-class-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="a5c63-112">For more information about registration, see [Registering NDF Helper Class Extensions](registering-ndf-helper-class-extensions.md).</span></span>

 

## <a name="rnwf-extensible-helper-class"></a><span data-ttu-id="a5c63-113">Расширяемый вспомогательный класс РНВФ</span><span class="sxs-lookup"><span data-stu-id="a5c63-113">RNWF Extensible Helper Class</span></span>

<span data-ttu-id="a5c63-114">Имя родительского класса вспомогательных классов</span><span class="sxs-lookup"><span data-stu-id="a5c63-114">Parent Helper Class Name</span></span>

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

<span data-ttu-id="a5c63-115">Пересмотренный расширяемый вспомогательный класс WiFi (РНВФ) является родительским для сторонних вспомогательных классов, которые позволяют диагностировать проблемы, связанные с расширенными протоколами 802,11, используемыми встроенным WiFi.</span><span class="sxs-lookup"><span data-stu-id="a5c63-115">The Revised Native Wifi (RNWF) extensible helper class is the parent for third-party helper classes that diagnose issues related to extending 802.11 protocols used by Native Wifi.</span></span>

<span data-ttu-id="a5c63-116">Двумя ключевыми атрибутами, предоставляемыми вспомогательным классом РНВФ, являются идентификаторы GUID интерфейса, где возникла ошибка, и контекст соединения.</span><span class="sxs-lookup"><span data-stu-id="a5c63-116">The two key attributes provided by the RNWF helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="a5c63-117">GUID интерфейса: этот атрибут называется "идентификатор интерфейса" и имеет тип **по \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="a5c63-117">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="a5c63-118">Контекст подключения: этот атрибут называется Network ID и имеет тип в \_ строке октета \_ .</span><span class="sxs-lookup"><span data-stu-id="a5c63-118">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="a5c63-119">Эта строка фактически является буфером \_ \_ структуры идентификатора беспроводной сети IHV вдиаг, \_ определенной в вланихв. h.</span><span class="sxs-lookup"><span data-stu-id="a5c63-119">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in Wlanihv.h.</span></span> <span data-ttu-id="a5c63-120">Эта структура определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a5c63-120">This structure is defined as follows.</span></span>

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> <span data-ttu-id="a5c63-121">**Вдиаг \_ \_Флаг идентификатора беспроводной сети IHV, \_ \_ \_ \_ Включенный параметр безопасность** — это единственное возможное значение **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="a5c63-121">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="a5c63-122">Атрибут сопоставления для вспомогательного класса стороннего производителя должен совпадать с ИДЕНТИФИКАТОРом службы соответствующего программного модуля.</span><span class="sxs-lookup"><span data-stu-id="a5c63-122">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="a5c63-123">Это также то же имя, что и сторонние лица, регистрируемые в реестре.</span><span class="sxs-lookup"><span data-stu-id="a5c63-123">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="a5c63-124">Диагностика беспроводных сетей будет запрашивать идентификатор службы во время беспроводного сеанса, в котором возникла эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="a5c63-124">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="a5c63-125">Информация будет возвращена NDF, который определит, имеется ли сторонний вспомогательный класс, а затем вызвать его.</span><span class="sxs-lookup"><span data-stu-id="a5c63-125">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="a5c63-126">В следующей таблице перечислены атрибуты, соответствующие расширенному вспомогательному классу РНВФ.</span><span class="sxs-lookup"><span data-stu-id="a5c63-126">The following table lists the matching attributes for the RNWF extensible helper class.</span></span>



| <span data-ttu-id="a5c63-127">Имя</span><span class="sxs-lookup"><span data-stu-id="a5c63-127">Name</span></span>          | <span data-ttu-id="a5c63-128">Тип</span><span class="sxs-lookup"><span data-stu-id="a5c63-128">Type</span></span>    | <span data-ttu-id="a5c63-129">Значение</span><span class="sxs-lookup"><span data-stu-id="a5c63-129">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="a5c63-130">диагностиксид</span><span class="sxs-lookup"><span data-stu-id="a5c63-130">DiagnosticsID</span></span> | <span data-ttu-id="a5c63-131">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a5c63-131">REG\_SZ</span></span> | <span data-ttu-id="a5c63-132">\[\_Строка GUID \_ диагностиксид</span><span class="sxs-lookup"><span data-stu-id="a5c63-132">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="l2security-extensible-helper-class"></a><span data-ttu-id="a5c63-133">Расширяемый вспомогательный класс L2Security</span><span class="sxs-lookup"><span data-stu-id="a5c63-133">L2Security Extensible Helper Class</span></span>

<span data-ttu-id="a5c63-134">Имя родительского класса вспомогательных классов</span><span class="sxs-lookup"><span data-stu-id="a5c63-134">Parent Helper Class Name</span></span>

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

<span data-ttu-id="a5c63-135">Расширяемый вспомогательный класс уровня 2 безопасности (L2Security) является родительским для сторонних вспомогательных классов, которые позволяют диагностировать проблемы, связанные с соответствующими службами и программными модулями, которые заменяют функции безопасности уровня 2.</span><span class="sxs-lookup"><span data-stu-id="a5c63-135">The Layer 2 Security (L2Security) extensible helper class is the parent for third-party helper classes that diagnose issues related to corresponding services and software modules that replace Layer 2 Security functionality.</span></span>

<span data-ttu-id="a5c63-136">Двумя ключевыми атрибутами, предоставляемыми вспомогательным классом уровня 2, является идентификатор GUID интерфейса, где возникла ошибка, и контекст соединения.</span><span class="sxs-lookup"><span data-stu-id="a5c63-136">The two key attributes provided by the Layer 2 Security helper class are the GUID of the interface where the issue occurred, and the connection context.</span></span>

-   <span data-ttu-id="a5c63-137">GUID интерфейса: этот атрибут называется "идентификатор интерфейса" и имеет тип **по \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="a5c63-137">Interface GUID: This attribute is named "Interface ID" and is of type **AT\_GUID**.</span></span>

-   <span data-ttu-id="a5c63-138">Контекст подключения: этот атрибут называется Network ID и имеет тип в \_ строке октета \_ .</span><span class="sxs-lookup"><span data-stu-id="a5c63-138">Connection Context: This attribute is named Network ID and is of type AT\_OCTET\_STRING.</span></span> <span data-ttu-id="a5c63-139">Эта строка фактически является буфером \_ \_ структуры идентификатора беспроводной сети IHV вдиаг, \_ определенной в вланихв. h.</span><span class="sxs-lookup"><span data-stu-id="a5c63-139">This string is actually a buffer the WDIAG\_IHV\_WLAN\_ID structure defined in wlanihv.h.</span></span> <span data-ttu-id="a5c63-140">Эта структура определяется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a5c63-140">This structure is defined as follows.</span></span>

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> <span data-ttu-id="a5c63-141">**Вдиаг \_ \_Флаг идентификатора беспроводной сети IHV, \_ \_ \_ \_ Включенный параметр безопасность** — это единственное возможное значение **dwFlags** .</span><span class="sxs-lookup"><span data-stu-id="a5c63-141">**WDIAG\_IHV\_WLAN\_ID\_FLAG\_SECURITY\_ENABLED** is the only possible **dwFlags** value.</span></span>

 

<span data-ttu-id="a5c63-142">Атрибут сопоставления для вспомогательного класса стороннего производителя должен совпадать с ИДЕНТИФИКАТОРом службы соответствующего программного модуля.</span><span class="sxs-lookup"><span data-stu-id="a5c63-142">The matching attribute for the third-party helper class should be the same as its corresponding software module's service ID.</span></span> <span data-ttu-id="a5c63-143">Это также то же имя, что и сторонние лица, регистрируемые в реестре.</span><span class="sxs-lookup"><span data-stu-id="a5c63-143">This is also the same name the third-party should be registered in the registry.</span></span> <span data-ttu-id="a5c63-144">Диагностика беспроводных сетей будет запрашивать идентификатор службы во время беспроводного сеанса, в котором возникла эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="a5c63-144">Wireless diagnostics will query the service ID during the wireless session in which the issue occurred.</span></span> <span data-ttu-id="a5c63-145">Информация будет возвращена NDF, который определит, имеется ли сторонний вспомогательный класс, а затем вызвать его.</span><span class="sxs-lookup"><span data-stu-id="a5c63-145">The information will be returned to NDF, which will determine whether the third-party helper class is present and registered, and then call it.</span></span>

<span data-ttu-id="a5c63-146">В следующей таблице перечислены атрибуты, соответствующие расширенному вспомогательному классу уровня 2 безопасности.</span><span class="sxs-lookup"><span data-stu-id="a5c63-146">The following table lists the matching attributes for the Layer 2 Security extensible helper class.</span></span>



| <span data-ttu-id="a5c63-147">Имя</span><span class="sxs-lookup"><span data-stu-id="a5c63-147">Name</span></span>          | <span data-ttu-id="a5c63-148">Тип</span><span class="sxs-lookup"><span data-stu-id="a5c63-148">Type</span></span>    | <span data-ttu-id="a5c63-149">Значение</span><span class="sxs-lookup"><span data-stu-id="a5c63-149">Value</span></span>                         |
|---------------|---------|-------------------------------|
| <span data-ttu-id="a5c63-150">диагностиксид</span><span class="sxs-lookup"><span data-stu-id="a5c63-150">DiagnosticsID</span></span> | <span data-ttu-id="a5c63-151">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a5c63-151">REG\_SZ</span></span> | <span data-ttu-id="a5c63-152">\[\_Строка GUID \_ диагностиксид</span><span class="sxs-lookup"><span data-stu-id="a5c63-152">\[DiagnosticsID\_GUID\_String</span></span> |



 

## <a name="matching-attributes"></a><span data-ttu-id="a5c63-153">Сопоставление атрибутов</span><span class="sxs-lookup"><span data-stu-id="a5c63-153">Matching Attributes</span></span>

<span data-ttu-id="a5c63-154">**диагностиксид**</span><span class="sxs-lookup"><span data-stu-id="a5c63-154">**DiagnosticsID**</span></span>

<span data-ttu-id="a5c63-155">802,11. Диагностика беспроводных сетей будет запрашивать *диагностиксид* из основной собственной службы Wi-Fi, чтобы узнать, установлены ли сторонние расширения беспроводной связи или модули безопасности, участвующие в подключении.</span><span class="sxs-lookup"><span data-stu-id="a5c63-155">802.11 Wireless Diagnostics will query the *DiagnosticsID* from the core Native Wifi service in order to find out if any third-party wireless extensions or security modules are installed and involved in the connection.</span></span> <span data-ttu-id="a5c63-156">После этого диагностика беспроводной сети предоставит эти данные этим вспомогательным классам сторонних поставщиков, используя *диагностиксид* в качестве соответствующего атрибута.</span><span class="sxs-lookup"><span data-stu-id="a5c63-156">Wireless Diagnostics will then provide hypotheses to these third-party helper classes using the *DiagnosticsID* as the matching attribute.</span></span> <span data-ttu-id="a5c63-157">Любые вспомогательные классы сторонних разработчиков должны включаться в и устанавливаться вместе с соответствующим пакетом драйверов.</span><span class="sxs-lookup"><span data-stu-id="a5c63-157">Any third-party helper classes should be included in and installed with the associated driver package.</span></span> <span data-ttu-id="a5c63-158">*Диагностиксид* будет ОПРЕДЕЛЕН в INF-файле минипорта как раздел реестра в директиве [аддрег](https://msdn.microsoft.com/library/ms794514.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a5c63-158">The *DiagnosticsID* will be defined in the miniport INF file as a registry key in the [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) directive.</span></span>

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

<span data-ttu-id="a5c63-159">Этот ключ определяет идентификатор вспомогательного класса беспроводной связи для программного модуля стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="a5c63-159">This key defines the ID of the wireless helper class for the third-party software module.</span></span> <span data-ttu-id="a5c63-160">Этот ключ является необязательным для платформы расширяемости, но он необходим, если реализация включает в себя вспомогательный класс беспроводных сетей, который подключается к NDF и может диагностировать проблемы подключения, связанные с модулями беспроводных сетей и безопасности РНВФ.</span><span class="sxs-lookup"><span data-stu-id="a5c63-160">This key is optional for the extensibility framework, but it is needed if the implementation includes an IHV Wireless Helper Class that plugs into NDF and can diagnose connectivity problems related to the RNWF wireless or security extensions.</span></span> <span data-ttu-id="a5c63-161">Вспомогательные классы диагностики MS WLAN запрашивают этот идентификатор из службы автоматической настройки беспроводной сети при установке модулей IHV и предоставляют этот идентификатор в качестве ссылки или сопоставления атрибута NDF во время сеанса диагностики, чтобы NDF мог вызвать соответствующий сторонний вспомогательный класс беспроводных сетей при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a5c63-161">MS WLAN diagnostics helper classes will query this ID from the Wireless Auto Configuration Service when IHV modules are installed and will provide this ID as the reference or matching attribute to NDF during a diagnostics session so that NDF can call the appropriate third-party wireless helper class when necessary.</span></span>

<span data-ttu-id="a5c63-162">**\[\_Строка GUID \_ диагностиксид\]**</span><span class="sxs-lookup"><span data-stu-id="a5c63-162">**\[DiagnosticsID\_GUID\_String\]**</span></span>

<span data-ttu-id="a5c63-163">Это значение должно быть строкой из всех прописных букв.</span><span class="sxs-lookup"><span data-stu-id="a5c63-163">This value must be a string of all uppercase letters.</span></span> <span data-ttu-id="a5c63-164">Например, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span><span class="sxs-lookup"><span data-stu-id="a5c63-164">For example, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".</span></span>

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a><span data-ttu-id="a5c63-165">Область действия вспомогательных классов диагностики беспроводной сети 802,11</span><span class="sxs-lookup"><span data-stu-id="a5c63-165">Scope of 802.11 Wireless Diagnostics Helper Classes</span></span>

<span data-ttu-id="a5c63-166">802,11. вспомогательные классы диагностики беспроводной связи в настоящее время диагностировать Беспроводные проблемы в следующих областях.</span><span class="sxs-lookup"><span data-stu-id="a5c63-166">802.11 wireless diagnostics helper classes currently diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="a5c63-167">Все проблемы с подключением 802,11, включая сопоставление 802,11, 802,11, 802,11 параметры безопасности, связанные с стандартом 802,11, & протоколы, изначально поддерживаемые в операционной системе, и проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="a5c63-167">Any 802.11 connectivity issues including 802.11 association, 802.11 authentication, 802.11 security settings related to 802.11 standards & protocols natively supported in the operating system, and performance issues.</span></span>
-   <span data-ttu-id="a5c63-168">Проблемы безопасности уровня 2 в отношении конфигураций 802.1 x и любых проблем, связанных с проверкой подлинности уровня 2, с помощью методов, изначально поддерживаемых в Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="a5c63-168">Layer 2 Security issues with regards to 802.1x configurations and any issues related to layer 2 authentication using methods natively supported on Windows Vista and Windows Server 2008.</span></span>
-   <span data-ttu-id="a5c63-169">Конфигурация не соответствует параметрам профиля между клиентом и точкой доступа или сетевой инфраструктурой и службами.</span><span class="sxs-lookup"><span data-stu-id="a5c63-169">Configuration mismatches in profile settings between the client and the Access Point or the network infrastructure and services.</span></span>

<span data-ttu-id="a5c63-170">802,11. вспомогательные классы диагностики беспроводной связи в настоящее время не выполняют диагностику беспроводных проблем в следующих областях.</span><span class="sxs-lookup"><span data-stu-id="a5c63-170">802.11 wireless diagnostics helper classes currently do not diagnose wireless issues in the following areas.</span></span>

-   <span data-ttu-id="a5c63-171">Проблемы, относящиеся к сторонним расширениям 802,11, включая любые параметры профиля или драйвера, связанные с этими расширениями.</span><span class="sxs-lookup"><span data-stu-id="a5c63-171">Issues related to third-party 802.11 extensions including any profile or driver settings related to these extensions.</span></span>
-   <span data-ttu-id="a5c63-172">Проблемы, связанные с методами EAP сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="a5c63-172">Issues related to third-party EAP methods.</span></span>
-   <span data-ttu-id="a5c63-173">Проблемы с драйвером минипорта беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="a5c63-173">Wireless miniport driver issues.</span></span>
-   <span data-ttu-id="a5c63-174">Любой протокол безопасности 802,11 и 2, а также проблемы, связанные со стандартами, которые изначально не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a5c63-174">Any 802.11 and layer 2 security protocol or standards-related issues that are not natively supported.</span></span>
-   <span data-ttu-id="a5c63-175">Проблемы на уровне системы или компонентов, которые могут повлиять на беспроводное подключение, такие как управление питанием, нехватка дискового пространства, состояние памяти и проблемы с оборудованием.</span><span class="sxs-lookup"><span data-stu-id="a5c63-175">System or component-level issues that might impact wireless connectivity, such as power management, low disk space, memory conditions, and hardware problems.</span></span>

<span data-ttu-id="a5c63-176">Кроме того, 802,11 Диагностика беспроводных сетей не анализирует случаи [**состояние highutilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) .</span><span class="sxs-lookup"><span data-stu-id="a5c63-176">Additionally, 802.11 Wireless Diagnostics does not analyze [**HighUtilization**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) cases.</span></span> <span data-ttu-id="a5c63-177">Выявленные проблемы производительности беспроводных сетей будут проанализированы и передаваться в качестве случаев [**ловхеалс**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .</span><span class="sxs-lookup"><span data-stu-id="a5c63-177">Identified wireless performance issues will be analyzed and reported as [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) cases.</span></span>

 

 




