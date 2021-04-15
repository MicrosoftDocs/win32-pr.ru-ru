---
title: Сообщение TDM_CLICK_BUTTON (Коммктрл. h)
description: Имитирует действие нажатия кнопки в диалоговом окне задачи.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- Элементы управления Windows для TDM_CLICK_BUTTON сообщений
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654509"
---
# <a name="tdm_click_button-message"></a><span data-ttu-id="d8325-104">Сообщение о нажатии \_ \_ кнопки TDM</span><span class="sxs-lookup"><span data-stu-id="d8325-104">TDM\_CLICK\_BUTTON message</span></span>

<span data-ttu-id="d8325-105">Имитирует действие нажатия кнопки в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="d8325-105">Simulates the action of a button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="d8325-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d8325-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8325-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8325-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8325-108">Значение **типа int** , указывающее идентификатор кнопки, которую необходимо щелкнуть.</span><span class="sxs-lookup"><span data-stu-id="d8325-108">An **int** that specifies the ID of the button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="d8325-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d8325-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8325-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d8325-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8325-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d8325-111">Return value</span></span>

<span data-ttu-id="d8325-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d8325-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8325-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d8325-113">Remarks</span></span>

<span data-ttu-id="d8325-114">Идентификатор кнопки, заданный параметром *wParam* , отправляется в функцию обратного вызова [**таскдиалогкаллбаккпрок**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) как часть [кнопки ТДН, которая \_ \_ щелкнула](tdn-button-clicked.md) код уведомления.</span><span class="sxs-lookup"><span data-stu-id="d8325-114">The button ID specified by *wParam* is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_BUTTON\_CLICKED](tdn-button-clicked.md) notification code.</span></span> <span data-ttu-id="d8325-115">После возврата функции обратного вызова диалоговое окно задачи закрывается, если в \_ функции обратного вызова было возвращено значение S ОК.</span><span class="sxs-lookup"><span data-stu-id="d8325-115">After the callback function returns, the task dialog is closed if S\_OK was returned from the callback function.</span></span> <span data-ttu-id="d8325-116">Если в \_ функции обратного вызова был возвращен параметр S false, диалоговое окно задачи остается активным.</span><span class="sxs-lookup"><span data-stu-id="d8325-116">If S\_FALSE was returned from the callback function, the task dialog remains active.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8325-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d8325-117">Requirements</span></span>



| <span data-ttu-id="d8325-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d8325-118">Requirement</span></span> | <span data-ttu-id="d8325-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d8325-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8325-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8325-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d8325-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8325-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d8325-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8325-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d8325-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8325-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d8325-124">Header</span><span class="sxs-lookup"><span data-stu-id="d8325-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8325-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8325-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

