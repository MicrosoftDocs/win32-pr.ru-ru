---
title: Сообщение CBEM_HASEDITCHANGED (Коммктрл. h)
description: Определяет, изменил ли пользователь текст элемента управления "поле ввода" ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- Элементы управления Windows для CBEM_HASEDITCHANGED сообщений
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989379"
---
# <a name="cbem_haseditchanged-message"></a><span data-ttu-id="a22d0-104">\_Сообщение кбем хаседитчанжед</span><span class="sxs-lookup"><span data-stu-id="a22d0-104">CBEM\_HASEDITCHANGED message</span></span>

<span data-ttu-id="a22d0-105">Определяет, изменил ли пользователь текст элемента управления "поле ввода" ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="a22d0-105">Determines whether the user has changed the text of a ComboBoxEx edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a22d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a22d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a22d0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a22d0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a22d0-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a22d0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a22d0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a22d0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a22d0-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="a22d0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a22d0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a22d0-111">Return value</span></span>

<span data-ttu-id="a22d0-112">Возвращает **значение true** , если текст в поле редактирования элемента управления был изменен, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a22d0-112">Returns **TRUE** if the text in the control's edit box has been changed, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a22d0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a22d0-113">Remarks</span></span>

<span data-ttu-id="a22d0-114">Элемент управления ComboBoxEx использует элемент управления "поле ввода", если для него задан стиль [**\_ раскрывающегося списка CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a22d0-114">A ComboBoxEx control uses an edit box control when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="a22d0-115">Вы можете получить маркер окна элемента управления "поле ввода", отправив сообщение [**кбем \_ жетедитконтрол**](cbem-geteditcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="a22d0-115">You can retrieve the edit box control's window handle by sending a [**CBEM\_GETEDITCONTROL**](cbem-geteditcontrol.md) message.</span></span>

<span data-ttu-id="a22d0-116">Когда пользователь начинает правку, вы получите уведомление о [кбен \_ BEGINEDIT](cben-beginedit.md) .</span><span class="sxs-lookup"><span data-stu-id="a22d0-116">When the user begins editing, you will receive a [CBEN\_BEGINEDIT](cben-beginedit.md) notification.</span></span> <span data-ttu-id="a22d0-117">Когда редактирование будет завершено или фокус изменится, вы получите уведомление [кбен \_ ENDEDIT](cben-endedit.md) .</span><span class="sxs-lookup"><span data-stu-id="a22d0-117">When editing is complete, or the focus changes, you will receive a [CBEN\_ENDEDIT](cben-endedit.md) notification.</span></span> <span data-ttu-id="a22d0-118">Сообщение **кбем \_ хаседитчанжед** полезно для определения того, был ли изменен текст, если он был отправлен перед \_ уведомлением кбен ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="a22d0-118">The **CBEM\_HASEDITCHANGED** message is only useful for determining whether the text has been changed if it is sent before the CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="a22d0-119">Если после этого сообщение будет отправлено, возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="a22d0-119">If the message is sent afterward, it will return **FALSE**.</span></span> <span data-ttu-id="a22d0-120">Например, предположим, что пользователь начинает редактировать текст в поле ввода, но меняет фокус, создавая КБЕН \_ ENDEDIT уведомление.</span><span class="sxs-lookup"><span data-stu-id="a22d0-120">For example, suppose the user starts to edit the text in the edit box but changes focus, generating a CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="a22d0-121">Если затем отправить сообщение **кбем \_ хаседитчанжед** , будет возвращено **значение false**, даже если текст был изменен.</span><span class="sxs-lookup"><span data-stu-id="a22d0-121">If you then send a **CBEM\_HASEDITCHANGED** message, it will return **FALSE**, even though the text has been changed.</span></span>

<span data-ttu-id="a22d0-122">[**\_ Простой стиль CBS**](combo-box-styles.md) работает неправильно с **кбем \_ хаседитчанжед**.</span><span class="sxs-lookup"><span data-stu-id="a22d0-122">The [**CBS\_SIMPLE**](combo-box-styles.md) style does not work correctly with **CBEM\_HASEDITCHANGED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a22d0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a22d0-123">Requirements</span></span>



| <span data-ttu-id="a22d0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a22d0-124">Requirement</span></span> | <span data-ttu-id="a22d0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a22d0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a22d0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a22d0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a22d0-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a22d0-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a22d0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a22d0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a22d0-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a22d0-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a22d0-130">Header</span><span class="sxs-lookup"><span data-stu-id="a22d0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a22d0-131"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a22d0-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





