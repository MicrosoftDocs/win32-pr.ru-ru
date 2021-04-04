---
title: Код уведомления TDN_HYPERLINK_CLICKED (Коммктрл. h)
description: Отправляется диалоговым окном задачи, когда пользователь щелкает гиперссылку в содержимом диалогового окна задачи. Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода Таскдиалогиндирект.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- TDN_HYPERLINK_CLICKED кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137602"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a><span data-ttu-id="8f31e-105">\_ \_ Код уведомления щелчка по ГИПЕРССЫЛКе ТДН</span><span class="sxs-lookup"><span data-stu-id="8f31e-105">TDN\_HYPERLINK\_CLICKED notification code</span></span>

<span data-ttu-id="8f31e-106">Отправляется диалоговым окном задачи, когда пользователь щелкает гиперссылку в содержимом диалогового окна задачи.</span><span class="sxs-lookup"><span data-stu-id="8f31e-106">Sent by a task dialog when the user clicks a hyperlink in the task dialog content.</span></span> <span data-ttu-id="8f31e-107">Этот код уведомления получается только через функцию обратного вызова диалогового окна задачи, которую можно зарегистрировать с помощью метода [**таскдиалогиндирект**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="8f31e-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="8f31e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f31e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f31e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f31e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f31e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8f31e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8f31e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f31e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f31e-112">Указатель на строку расширенных символов, содержащую URL-адрес гиперссылки.</span><span class="sxs-lookup"><span data-stu-id="8f31e-112">Pointer to a wide-character string containing the URL of the hyperlink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f31e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8f31e-113">Return value</span></span>

<span data-ttu-id="8f31e-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8f31e-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f31e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8f31e-115">Requirements</span></span>



| <span data-ttu-id="8f31e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="8f31e-116">Requirement</span></span> | <span data-ttu-id="8f31e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8f31e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f31e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8f31e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8f31e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f31e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f31e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8f31e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8f31e-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8f31e-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f31e-122">Header</span><span class="sxs-lookup"><span data-stu-id="8f31e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f31e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f31e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





