---
description: Событие, возникающее при успешном завершении обмена данными.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Событие WIA. Онтрансферкомплете
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264538"
---
# <a name="wiaontransfercomplete-event"></a><span data-ttu-id="1399c-103">Событие WIA. Онтрансферкомплете</span><span class="sxs-lookup"><span data-stu-id="1399c-103">Wia.OnTransferComplete event</span></span>

<span data-ttu-id="1399c-104">Событие, возникающее при успешном завершении обмена данными.</span><span class="sxs-lookup"><span data-stu-id="1399c-104">Event that occurs when a data transfer is completed successfully.</span></span>

## <a name="syntax"></a><span data-ttu-id="1399c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1399c-105">Syntax</span></span>


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="1399c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1399c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1399c-107">*Элемент*</span><span class="sxs-lookup"><span data-stu-id="1399c-107">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="1399c-108">Объект [**Item**](-wia-item.md) передан.</span><span class="sxs-lookup"><span data-stu-id="1399c-108">The [**Item**](-wia-item.md) object transferred.</span></span>

</dd> <dt>

<span data-ttu-id="1399c-109">*Путь*</span><span class="sxs-lookup"><span data-stu-id="1399c-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="1399c-110">Путь и имя переданного образа.</span><span class="sxs-lookup"><span data-stu-id="1399c-110">The path and file name of the transferred image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1399c-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1399c-111">Return value</span></span>

<span data-ttu-id="1399c-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1399c-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1399c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1399c-113">Remarks</span></span>

<span data-ttu-id="1399c-114">WIA уведомляет сценарий или приложение об успешном завершении перемещения данных, изображения или звука.</span><span class="sxs-lookup"><span data-stu-id="1399c-114">WIA notifies the script or application when a data transfer, image or sound, completes successfully.</span></span> <span data-ttu-id="1399c-115">Реализуйте  \_ подпрограммы обжвиа **онтрансферкомплете ()** , чтобы сценарий или приложение отвечали на завершение передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="1399c-115">Implement the **objWia**\_**OnTransferComplete()** subroutine to allow your script or application to respond to the completion of the data transfer.</span></span>

<span data-ttu-id="1399c-116">Например, может потребоваться, чтобы сценарий отображал изображение после его передачи.</span><span class="sxs-lookup"><span data-stu-id="1399c-116">For example, you might want a script to display an image after it is transferred.</span></span>

## <a name="requirements"></a><span data-ttu-id="1399c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1399c-117">Requirements</span></span>



| <span data-ttu-id="1399c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1399c-118">Requirement</span></span> | <span data-ttu-id="1399c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1399c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1399c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1399c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1399c-121">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1399c-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1399c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1399c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1399c-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1399c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1399c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1399c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1399c-125"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="1399c-125"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




