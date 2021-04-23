---
description: Используется приложениями для вывода пользователем диалогового окна устройства.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: Функция Девицедиалог (Виадевд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105693078"
---
# <a name="devicedialog-function"></a><span data-ttu-id="9671d-103">Функция Девицедиалог</span><span class="sxs-lookup"><span data-stu-id="9671d-103">DeviceDialog function</span></span>

<span data-ttu-id="9671d-104">Используется приложениями для вывода пользователем диалогового окна устройства.</span><span class="sxs-lookup"><span data-stu-id="9671d-104">Used by applications to display a device dialog box to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="9671d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9671d-105">Syntax</span></span>


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="9671d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9671d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9671d-107">*пдевицедиалогдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9671d-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9671d-108">Тип: **пдевицедиалогдата**</span><span class="sxs-lookup"><span data-stu-id="9671d-108">Type: **PDEVICEDIALOGDATA**</span></span>

<span data-ttu-id="9671d-109">[**Девицедиалогдата**](-wia-devicedialogdata.md) , используемый для создания диалогового окна устройства.</span><span class="sxs-lookup"><span data-stu-id="9671d-109">The [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) to use to create the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9671d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9671d-110">Return value</span></span>

<span data-ttu-id="9671d-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9671d-111">Type: **HRESULT**</span></span>

<span data-ttu-id="9671d-112">Если эта функция завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="9671d-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9671d-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9671d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9671d-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9671d-114">Requirements</span></span>



| <span data-ttu-id="9671d-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9671d-115">Requirement</span></span> | <span data-ttu-id="9671d-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9671d-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9671d-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9671d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9671d-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9671d-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9671d-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9671d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9671d-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9671d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9671d-121">Header</span><span class="sxs-lookup"><span data-stu-id="9671d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9671d-122"><dt>Виадевд. h</dt></span><span class="sxs-lookup"><span data-stu-id="9671d-122"><dt>Wiadevd.h</dt></span></span> </dl>   |
| <span data-ttu-id="9671d-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9671d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9671d-124"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9671d-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9671d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9671d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9671d-126">**девицедиалогдата**</span><span class="sxs-lookup"><span data-stu-id="9671d-126">**DEVICEDIALOGDATA**</span></span>](-wia-devicedialogdata.md)
</dt> </dl>

 

 




