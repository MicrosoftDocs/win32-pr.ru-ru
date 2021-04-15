---
title: DRM_SAPLEVEL (не рекомендуется)
description: Указывает уровень защищенного звукового пути (SAP), поддерживаемый приложением.
ms.assetid: a2648083-f9ec-43c7-96c8-4d8b5f8285d1
keywords:
- DRM_SAPLEVEL (не рекомендуется) формат Windows Media
topic_type:
- apiref
api_name:
- DRM_SAPLEVEL (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43711c6c394761f599271809419a46311265d8b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647901"
---
# <a name="drm_saplevel-deprecated"></a><span data-ttu-id="f4c17-104">DRM \_ саплевел (не рекомендуется)</span><span class="sxs-lookup"><span data-stu-id="f4c17-104">DRM\_SAPLEVEL (deprecated)</span></span>

<span data-ttu-id="f4c17-105">\[**DRM \_ САПЛЕВЕЛ** больше не доступен для использования в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f4c17-105">\[**DRM\_SAPLEVEL** is no longer available for use as of Windows Vista.</span></span> <span data-ttu-id="f4c17-106">Вместо этого используйте звук защищенного пользовательского режима (PUMA) в библиотеке Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="f4c17-106">Instead, use Protected User Mode Audio (PUMA) in the Media Foundation library.</span></span> <span data-ttu-id="f4c17-107">\]</span><span class="sxs-lookup"><span data-stu-id="f4c17-107">\]</span></span>

<span data-ttu-id="f4c17-108">Свойство **DRM \_ саплевел** указывает уровень защищенного звукового пути (SAP), поддерживаемого приложением.</span><span class="sxs-lookup"><span data-stu-id="f4c17-108">The **DRM\_SAPLEVEL** property specifies the secure audio path (SAP) level supported by your application.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f4c17-109">Глобальная константа</span><span class="sxs-lookup"><span data-stu-id="f4c17-109">Global Constant</span></span>

<span data-ttu-id="f4c17-110">g \_ всзвмдрм \_ саплевел</span><span class="sxs-lookup"><span data-stu-id="f4c17-110">g\_wszWMDRM\_SAPLEVEL</span></span>

## <a name="data-type"></a><span data-ttu-id="f4c17-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f4c17-111">Data Type</span></span>

<span data-ttu-id="f4c17-112">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="f4c17-112">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c17-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4c17-113">Remarks</span></span>

<span data-ttu-id="f4c17-114">Это свойство доступно только для записи и устанавливается путем вызова [**ивмдрмреадер:: сетдрмпроперти**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="f4c17-114">This is a write-only property that is set by calling [**IWMDRMReader::SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty).</span></span> <span data-ttu-id="f4c17-115">Значение представляет собой строковое представление уровня SAP с расширенными символами, например L "200".</span><span class="sxs-lookup"><span data-stu-id="f4c17-115">The value is a wide-character string representation of the SAP level, such as L"200".</span></span> <span data-ttu-id="f4c17-116">Текущие поддерживаемые значения: 200 и 300.</span><span class="sxs-lookup"><span data-stu-id="f4c17-116">Current supported values are 200 and 300.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c17-117">Требования</span><span class="sxs-lookup"><span data-stu-id="f4c17-117">Requirements</span></span>



| <span data-ttu-id="f4c17-118">Требование</span><span class="sxs-lookup"><span data-stu-id="f4c17-118">Requirement</span></span> | <span data-ttu-id="f4c17-119">Значение</span><span class="sxs-lookup"><span data-stu-id="f4c17-119">Value</span></span> |
|----------------------------------|--------------------------------|
| <span data-ttu-id="f4c17-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f4c17-120">End of client support</span></span><br/> | <span data-ttu-id="f4c17-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4c17-121">Windows XP</span></span><br/>          |
| <span data-ttu-id="f4c17-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f4c17-122">End of server support</span></span><br/> | <span data-ttu-id="f4c17-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f4c17-123">Windows Server 2003</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4c17-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4c17-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c17-125">**Свойства DRM**</span><span class="sxs-lookup"><span data-stu-id="f4c17-125">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 





