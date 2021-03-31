---
title: DRM_Level
description: '\_Уровень DRM — это атрибут лицензии, который задается пакетом SDK формата Windows Media при создании локальной лицензии для файлов, защищенных с помощью DRM версии 1.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level формат Windows Media
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336428"
---
# <a name="drm_level"></a><span data-ttu-id="98a21-104">\_Уровень DRM</span><span class="sxs-lookup"><span data-stu-id="98a21-104">DRM\_Level</span></span>

<span data-ttu-id="98a21-105">**DRM \_ Level** — это атрибут лицензии, который задается пакетом SDK формата Windows Media при создании локальной лицензии для файлов, защищенных с помощью DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="98a21-105">**DRM\_Level** is a license attribute that the Windows Media Format SDK sets when it creates a local license for files protected with DRM version 1.</span></span> <span data-ttu-id="98a21-106">Он содержит уровень безопасности, который должен иметь вызывающее приложение для доступа к содержимому в файле.</span><span class="sxs-lookup"><span data-stu-id="98a21-106">It contains the security level that the calling application must have to access the content in the file.</span></span> <span data-ttu-id="98a21-107">По умолчанию используется значение 150.</span><span class="sxs-lookup"><span data-stu-id="98a21-107">The default value is 150.</span></span>

## <a name="global-constant"></a><span data-ttu-id="98a21-108">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="98a21-108">Global Constant</span></span>

<span data-ttu-id="98a21-109">\_уровень g всзвмдрм \_</span><span class="sxs-lookup"><span data-stu-id="98a21-109">g\_wszWMDRM\_Level</span></span>

## <a name="data-type"></a><span data-ttu-id="98a21-110">Тип данных</span><span class="sxs-lookup"><span data-stu-id="98a21-110">Data Type</span></span>

<span data-ttu-id="98a21-111">**ВМТ, \_ тип \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="98a21-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="98a21-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98a21-112">Remarks</span></span>

<span data-ttu-id="98a21-113">Уровень безопасности DRM приложения определяется конкретной библиотекой вмстубдрм, на которую она ссылается во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="98a21-113">An application's DRM security level is determined by the particular wmstubdrm library that it links to at compile time.</span></span> <span data-ttu-id="98a21-114">Дополнительные сведения об этих уровнях безопасности см. [в разделе получение требуемой библиотеки DRM](obtaining-the-required-drm-library.md).</span><span class="sxs-lookup"><span data-stu-id="98a21-114">For more information on these security levels, see [Obtaining the Required DRM Library](obtaining-the-required-drm-library.md).</span></span> <span data-ttu-id="98a21-115">Используйте [**ивмхеадеринфо:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , чтобы задать это свойство при защите файлов ASF с помощью DRM версии 1.</span><span class="sxs-lookup"><span data-stu-id="98a21-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when protecting ASF files with DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="98a21-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98a21-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98a21-117">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="98a21-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




