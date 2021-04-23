---
description: Уведомляет панель приложений о том, что в контекстном меню панели задач выбрана команда каскадная, мозаичная или плитка по вертикали.
title: Сообщение ABN_WINDOWARRANGE (Шеллапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540586"
---
# <a name="abn_windowarrange-message"></a><span data-ttu-id="cf4d2-103">\_Сообщение АБН виндоварранже</span><span class="sxs-lookup"><span data-stu-id="cf4d2-103">ABN\_WINDOWARRANGE message</span></span>

<span data-ttu-id="cf4d2-104">Уведомляет панель приложений о том, что в контекстном меню панели задач выбрана команда каскадная, мозаичная или плитка по вертикали.</span><span class="sxs-lookup"><span data-stu-id="cf4d2-104">Notifies an appbar that the user has selected the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span>


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="cf4d2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf4d2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf4d2-106">*фбегиннинг*</span><span class="sxs-lookup"><span data-stu-id="cf4d2-106">*fBeginning*</span></span> 
</dt> <dd>

<span data-ttu-id="cf4d2-107">Флаг, указывающий, начинается ли операция Cascade или Tile.</span><span class="sxs-lookup"><span data-stu-id="cf4d2-107">A flag specifying whether the cascade or tile operation is beginning.</span></span> <span data-ttu-id="cf4d2-108">Этот параметр имеет **значение true** , если операция начинается, а окна еще не перемещены.</span><span class="sxs-lookup"><span data-stu-id="cf4d2-108">This parameter is **TRUE** if the operation is beginning and the windows have not yet been moved.</span></span> <span data-ttu-id="cf4d2-109">**Значение false** , если операция завершена.</span><span class="sxs-lookup"><span data-stu-id="cf4d2-109">It is **FALSE** if the operation has completed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf4d2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf4d2-110">Return value</span></span>

<span data-ttu-id="cf4d2-111">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="cf4d2-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf4d2-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="cf4d2-112">Remarks</span></span>

<span data-ttu-id="cf4d2-113">Система отправляет это сообщение с уведомлением дважды, если параметру *lParam* присвоено значение **true** , а параметру *lParam* присвоено значение **false**.</span><span class="sxs-lookup"><span data-stu-id="cf4d2-113">The system sends this notification message twice first with *lParam* set to **TRUE** and then with *lParam* set to **FALSE**.</span></span> <span data-ttu-id="cf4d2-114">Первое уведомление отправляется до каскадного или мозаичного разбиения окон, а второе отправляется после выполнения операции Cascade или плитки.</span><span class="sxs-lookup"><span data-stu-id="cf4d2-114">The first notification is sent before the windows are cascaded or tiled, and the second is sent after the cascade or tile operation has occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf4d2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cf4d2-115">Requirements</span></span>



| <span data-ttu-id="cf4d2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cf4d2-116">Requirement</span></span> | <span data-ttu-id="cf4d2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cf4d2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4d2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf4d2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4d2-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cf4d2-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cf4d2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf4d2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4d2-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cf4d2-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cf4d2-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cf4d2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf4d2-123"><dt>Шеллапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf4d2-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




