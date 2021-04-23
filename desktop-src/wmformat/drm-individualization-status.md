---
title: Перечисление DRM_INDIVIDUALIZATION_STATUS (Дрмекстерналс. h)
description: '\_Тип перечисления для индивидуальной защиты DRM \_ определяет допустимые состояния для индивидуальной защиты DRM. | Перечисление DRM_INDIVIDUALIZATION_STATUS (Дрмекстерналс. h)'
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Формат Windows Media DRM_INDIVIDUALIZATION_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424293"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a><span data-ttu-id="a055e-106">Перечисление DRM_INDIVIDUALIZATION_STATUS (Дрмекстерналс. h)</span><span class="sxs-lookup"><span data-stu-id="a055e-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="a055e-107">Тип перечисления для **\_ индивидуальной защиты DRM \_** определяет допустимые состояния для [*индивидуальной*](wmformat-glossary.md)защиты DRM.</span><span class="sxs-lookup"><span data-stu-id="a055e-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM [*individualization*](wmformat-glossary.md).</span></span> <span data-ttu-id="a055e-108">Когда приложение инициирует индивидуальную работу с помощью вызова [**ивмдрмреадер:: индивидуализируйте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), ход выполнения запроса на индивидуальную передачу передается приложению посредством вызовов метода [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="a055e-108">When an application initiates individualization with a call to [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), the progress of the individualization request is conveyed to the application through calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="a055e-109">Все сообщения о состоянии индивидуальной работы будут использовать \_ член ВМТ индивидуализируйте типа [**перечисления \_ ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) в качестве параметра *Status* .</span><span class="sxs-lookup"><span data-stu-id="a055e-109">Individualization status messages will all use the WMT\_INDIVIDUALIZE member of the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type as the *Status* parameter.</span></span> <span data-ttu-id="a055e-110">Состояние индивидуализации передается в **OnStatus** в параметре *pValue* .</span><span class="sxs-lookup"><span data-stu-id="a055e-110">The status of the individualization is passed to **OnStatus** in the *pValue* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a055e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a055e-111">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="a055e-112">Константы</span><span class="sxs-lookup"><span data-stu-id="a055e-112">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a055e-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**столбец indid не \_ определен**</span><span class="sxs-lookup"><span data-stu-id="a055e-113"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="a055e-114">Это значение зарезервировано для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="a055e-114">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="a055e-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**\_Начало indid**</span><span class="sxs-lookup"><span data-stu-id="a055e-115"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="a055e-116">Указывает начало процесса индивидуализации.</span><span class="sxs-lookup"><span data-stu-id="a055e-116">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="a055e-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**столбец indid \_ выполнен**</span><span class="sxs-lookup"><span data-stu-id="a055e-117"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="a055e-118">Указывает, что процесс индивидуализации завершен.</span><span class="sxs-lookup"><span data-stu-id="a055e-118">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="a055e-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**\_Ошибка indid**</span><span class="sxs-lookup"><span data-stu-id="a055e-119"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="a055e-120">Указывает, что процесс индивидуализации завершился ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a055e-120">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="a055e-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**\_Отмена indid**</span><span class="sxs-lookup"><span data-stu-id="a055e-121"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="a055e-122">Указывает, что процесс индивидуализации был отменен в результате вызова [**ивмдрмреадер:: канцелиндивидуализатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span><span class="sxs-lookup"><span data-stu-id="a055e-122">Indicates that the individualization process was canceled as the result of a call to [**IWMDRMReader::CancelIndividualization**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).</span></span>

</dd> <dt>

<span data-ttu-id="a055e-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**\_скачивание indid**</span><span class="sxs-lookup"><span data-stu-id="a055e-123"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="a055e-124">Указывает, что загружается обновление безопасности.</span><span class="sxs-lookup"><span data-stu-id="a055e-124">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="a055e-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**\_Установка indid**</span><span class="sxs-lookup"><span data-stu-id="a055e-125"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="a055e-126">Указывает, что устанавливается обновление системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="a055e-126">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a055e-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a055e-127">Remarks</span></span>

<span data-ttu-id="a055e-128">Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](wm-individualize-status.md) .</span><span class="sxs-lookup"><span data-stu-id="a055e-128">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a055e-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a055e-129">Requirements</span></span>



| <span data-ttu-id="a055e-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a055e-130">Requirement</span></span> | <span data-ttu-id="a055e-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a055e-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a055e-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a055e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a055e-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a055e-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a055e-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a055e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a055e-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a055e-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a055e-136">Версия</span><span class="sxs-lookup"><span data-stu-id="a055e-136">Version</span></span><br/>                  | <span data-ttu-id="a055e-137">Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK</span><span class="sxs-lookup"><span data-stu-id="a055e-137">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="a055e-138">Header</span><span class="sxs-lookup"><span data-stu-id="a055e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a055e-139"><dt>Дрмекстерналс. h</dt></span><span class="sxs-lookup"><span data-stu-id="a055e-139"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a055e-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a055e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a055e-141">**\_состояние HTTP \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="a055e-141">**DRM\_HTTP\_STATUS**</span></span>](drm-http-status.md)
</dt> <dt>

[<span data-ttu-id="a055e-142">**Типы перечислений**</span><span class="sxs-lookup"><span data-stu-id="a055e-142">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





