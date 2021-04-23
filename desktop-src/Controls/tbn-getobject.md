---
title: Код уведомления TBN_GETOBJECT (Коммктрл. h)
description: Отправляется элементом управления ToolBar, использующим стиль ТБСТИЛЕ \_ регистердроп для запроса целевого объекта перетаскивания, когда указатель проходит над одной из его кнопок. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135094"
---
# <a name="tbn_getobject-notification-code"></a><span data-ttu-id="2c47d-105">\_Код уведомления ТБН GetObject</span><span class="sxs-lookup"><span data-stu-id="2c47d-105">TBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="2c47d-106">Отправляется элементом управления ToolBar, использующим стиль [**тбстиле \_ регистердроп**](toolbar-control-and-button-styles.md) для запроса целевого объекта перетаскивания, когда указатель проходит над одной из его кнопок.</span><span class="sxs-lookup"><span data-stu-id="2c47d-106">Sent by a toolbar control that uses the [**TBSTYLE\_REGISTERDROP**](toolbar-control-and-button-styles.md) style to request a drop target object when the pointer passes over one of its buttons.</span></span> <span data-ttu-id="2c47d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2c47d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2c47d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2c47d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c47d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c47d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c47d-110">Указатель на структуру [**нмобжектнотифи**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) , которая содержит сведения о кнопке, передаваемой указателем, и получает данные, предоставляемые приложением в ответ на этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="2c47d-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the button that the pointer passed over and receives data the application provides in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c47d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2c47d-111">Return value</span></span>

<span data-ttu-id="2c47d-112">Приложение, обрабатывающее этот код уведомления, должно возвращать ноль.</span><span class="sxs-lookup"><span data-stu-id="2c47d-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c47d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c47d-113">Remarks</span></span>

<span data-ttu-id="2c47d-114">Чтобы предоставить объект, приложение должно задать значения в некоторых членах структуры [**нмобжектнотифи**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) при значении *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2c47d-114">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="2c47d-115">Элементу **объект** должен быть присвоен допустимый указатель на объект, а элементу **hResult** должен быть присвоен флаг Success.</span><span class="sxs-lookup"><span data-stu-id="2c47d-115">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="2c47d-116">Для обеспечения соответствия стандартам модели COM всегда увеличивать число ссылок объекта при предоставлении указателя на объект.</span><span class="sxs-lookup"><span data-stu-id="2c47d-116">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="2c47d-117">Если приложение не предоставляет объект, оно должно установить для **объект** **значение NULL** , а для **hResult** — флаг сбоя.</span><span class="sxs-lookup"><span data-stu-id="2c47d-117">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c47d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2c47d-118">Requirements</span></span>



| <span data-ttu-id="2c47d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2c47d-119">Requirement</span></span> | <span data-ttu-id="2c47d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2c47d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c47d-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c47d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2c47d-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c47d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c47d-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c47d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2c47d-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c47d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c47d-125">Header</span><span class="sxs-lookup"><span data-stu-id="2c47d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c47d-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c47d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





