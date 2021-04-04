---
title: Сообщение TDM_CLICK_RADIO_BUTTON (Коммктрл. h)
description: Имитирует действие переключателя щелкните в диалоговом окне задачи.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- Элементы управления Windows для TDM_CLICK_RADIO_BUTTON сообщений
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989286"
---
# <a name="tdm_click_radio_button-message"></a><span data-ttu-id="8adbc-104">TDM \_ щелкните \_ сообщение переключателя \_</span><span class="sxs-lookup"><span data-stu-id="8adbc-104">TDM\_CLICK\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="8adbc-105">Имитирует действие переключателя щелкните в диалоговом окне задачи.</span><span class="sxs-lookup"><span data-stu-id="8adbc-105">Simulates the action of a radio button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="8adbc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8adbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8adbc-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8adbc-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8adbc-108">Значение **типа int** , указывающее идентификатор переключателя, который следует щелкнуть.</span><span class="sxs-lookup"><span data-stu-id="8adbc-108">An **int** value that specifies the ID of the radio button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="8adbc-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8adbc-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8adbc-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8adbc-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8adbc-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8adbc-111">Return value</span></span>

<span data-ttu-id="8adbc-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8adbc-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="8adbc-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8adbc-113">Remarks</span></span>

<span data-ttu-id="8adbc-114">Указанный идентификатор переключателя отправляется в функцию обратного вызова [**таскдиалогкаллбаккпрок**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) в рамках [ \_ переключателя \_ \_ ТДН](tdn-radio-button-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="8adbc-114">The specified radio button ID is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_RADIO\_BUTTON\_CLICKED](tdn-radio-button-clicked.md) notification code.</span></span> <span data-ttu-id="8adbc-115">После возврата функции обратного вызова будет установлен переключатель.</span><span class="sxs-lookup"><span data-stu-id="8adbc-115">After the callback function returns, the radio button will be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="8adbc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="8adbc-116">Requirements</span></span>



| <span data-ttu-id="8adbc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="8adbc-117">Requirement</span></span> | <span data-ttu-id="8adbc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="8adbc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8adbc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8adbc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8adbc-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8adbc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8adbc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8adbc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8adbc-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8adbc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8adbc-123">Header</span><span class="sxs-lookup"><span data-stu-id="8adbc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8adbc-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8adbc-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

