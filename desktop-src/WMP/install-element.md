---
title: Элемент install
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. Использование этой функции вне контекста Интернет-магазина не поддерживается. Элемент Install указывает значения, используемые проигрывателем Windows Media для установки Интернет-магазина.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Установка элемента Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694659"
---
# <a name="install-element"></a><span data-ttu-id="9164b-106">Элемент install</span><span class="sxs-lookup"><span data-stu-id="9164b-106">Install Element</span></span>

> [!Note]  
> <span data-ttu-id="9164b-107">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="9164b-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="9164b-108">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9164b-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="9164b-109">Элемент **Install** указывает значения, используемые проигрывателем Windows Media для установки Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="9164b-109">The **Install** element specifies values used by Windows Media Player to install an online store.</span></span>

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="9164b-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9164b-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="9164b-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**Еулаурл** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="9164b-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="9164b-112">Полный URL-адрес для файла с расширением txt, используемым проигрывателем Windows Media для вывода лицензионного соглашения (EULA).</span><span class="sxs-lookup"><span data-stu-id="9164b-112">Fully qualified URL for a file with a .txt file name extension that Windows Media Player uses to display an End User License Agreement (EULA).</span></span> <span data-ttu-id="9164b-113">Этот файл должен быть закодирован в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9164b-113">This file must be encoded in ANSI format.</span></span>

</dd> <dt>

<span data-ttu-id="9164b-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**Кодеурл** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="9164b-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="9164b-115">Полный URL-адрес пакета с расширением CAB, который используется для установки Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="9164b-115">Fully qualified URL for a package, with a .cab file name extension, that is used to install the online store.</span></span> <span data-ttu-id="9164b-116">Пакет и все модули кода в пакете должны быть подписаны.</span><span class="sxs-lookup"><span data-stu-id="9164b-116">The package and all code modules in the package must be signed.</span></span> <span data-ttu-id="9164b-117">Сведения о подписывании кода см. в статье [Введение в подписывание кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) в библиотеке MSDN.</span><span class="sxs-lookup"><span data-stu-id="9164b-117">For information about code signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in the MSDN Library.</span></span>

</dd> <dt>

<span data-ttu-id="9164b-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**Привациинфаурл** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="9164b-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="9164b-119">Полный URL-адрес веб-страницы, содержащей сведения о политике конфиденциальности для Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="9164b-119">Fully qualified URL for a webpage that contains privacy policy information for the online store.</span></span>

</dd> <dt>

<span data-ttu-id="9164b-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**Инсталлапп** (обязательно)</span><span class="sxs-lookup"><span data-stu-id="9164b-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (required)</span></span>
</dt> <dd>

<span data-ttu-id="9164b-121">Имя запускаемого EXE-или INF-файла.</span><span class="sxs-lookup"><span data-stu-id="9164b-121">Name of the EXE or INF file to run.</span></span> <span data-ttu-id="9164b-122">Этот файл должен содержаться в CAB-файле, указанном атрибутом **кодеурл** .</span><span class="sxs-lookup"><span data-stu-id="9164b-122">This file must be contained in the CAB file specified by the **CodeURL** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="9164b-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**Инсталлдата** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="9164b-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="9164b-124">Строка командной строки, которая передается в приложение, указанное атрибутом **инсталлапп** .</span><span class="sxs-lookup"><span data-stu-id="9164b-124">Command-line string that is passed to the application specified by the **InstallApp** attribute.</span></span> <span data-ttu-id="9164b-125">Этот атрибут применим только в том случае, если значение параметра **инсталлапп** указывает исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="9164b-125">This attribute is only applicable when the value for **InstallApp** specifies an executable.</span></span>

</dd> <dt>

<span data-ttu-id="9164b-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**Каталогурл** (требуется для типа 1, игнорируется для типа 2)</span><span class="sxs-lookup"><span data-stu-id="9164b-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (required for type 1, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="9164b-127">Полный URL-адрес для скомпилированного каталога Интернет-магазина.</span><span class="sxs-lookup"><span data-stu-id="9164b-127">Fully qualified URL for the online store's compiled catalog.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="9164b-128">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9164b-128">Parent/Child Elements</span></span>



| <span data-ttu-id="9164b-129">Иерархия</span><span class="sxs-lookup"><span data-stu-id="9164b-129">Hierarchy</span></span>       | <span data-ttu-id="9164b-130">Элемент</span><span class="sxs-lookup"><span data-stu-id="9164b-130">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="9164b-131">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9164b-131">Parent elements</span></span> | <span data-ttu-id="9164b-132">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9164b-132">**ServiceInfo**</span></span> |
| <span data-ttu-id="9164b-133">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9164b-133">Child elements</span></span>  | <span data-ttu-id="9164b-134">Нет</span><span class="sxs-lookup"><span data-stu-id="9164b-134">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="9164b-135">Remarks</span><span class="sxs-lookup"><span data-stu-id="9164b-135">Remarks</span></span>

<span data-ttu-id="9164b-136">Если какой-либо из необходимых атрибутов отсутствует или недоступен, программа установки проигрывателя Windows Media не будет пытаться загрузить и установить код поставщика интерактивного магазина.</span><span class="sxs-lookup"><span data-stu-id="9164b-136">If any of the required attributes are missing or not available, Windows Media Player setup will not attempt to download and install the online store provider code.</span></span> <span data-ttu-id="9164b-137">Программа установки настроит значения автономного режима по умолчанию, как указано в документе **serviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="9164b-137">Setup will configure the offline default values as specified in the **ServiceInfo** document.</span></span> <span data-ttu-id="9164b-138">**ServiceInfo** можно использовать при отсутствии подключения к Интернету, передав имя поставщика по умолчанию и сведения о **serviceInfo** в качестве параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="9164b-138">**ServiceInfo** can be used when not connected to the Internet by passing the default provider name and the **ServiceInfo** information as command-line parameters.</span></span> <span data-ttu-id="9164b-139">Дополнительные сведения о параметрах командной строки см. в разделе [распространение программного обеспечения проигрывателя Windows Media](redistributing-windows-media-player-software.md) .</span><span class="sxs-lookup"><span data-stu-id="9164b-139">See [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) for details about command-line options.</span></span>

> [!Note]  
> <span data-ttu-id="9164b-140">Для использования этого элемента необходимо подписать соглашение о повторном распространении с помощью корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="9164b-140">Use of this element requires that you sign a redistribution agreement with Microsoft.</span></span> <span data-ttu-id="9164b-141">Для получения дополнительных сведений обратитесь к своему бизнес-представителям.</span><span class="sxs-lookup"><span data-stu-id="9164b-141">Contact your business representative for details.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9164b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="9164b-142">Requirements</span></span>



| <span data-ttu-id="9164b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="9164b-143">Requirement</span></span> | <span data-ttu-id="9164b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="9164b-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="9164b-145">Версия</span><span class="sxs-lookup"><span data-stu-id="9164b-145">Version</span></span><br/> | <span data-ttu-id="9164b-146">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="9164b-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9164b-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9164b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9164b-148">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="9164b-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="9164b-149">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="9164b-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="9164b-150">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="9164b-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

