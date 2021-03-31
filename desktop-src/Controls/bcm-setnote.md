---
title: Сообщение BCM_SETNOTE (Коммктрл. h)
description: Задает текст примечания, связанного с кнопкой ссылки на команду. Это сообщение можно отправить явным образом или воспользоваться \_ макросом кнопки сетноте.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- Элементы управления Windows для BCM_SETNOTE сообщений
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988643"
---
# <a name="bcm_setnote-message"></a><span data-ttu-id="cdaed-105">\_Сообщение СЕТНОТЕ BCM</span><span class="sxs-lookup"><span data-stu-id="cdaed-105">BCM\_SETNOTE message</span></span>

<span data-ttu-id="cdaed-106">Задает текст примечания, связанного с кнопкой ссылки на команду.</span><span class="sxs-lookup"><span data-stu-id="cdaed-106">Sets the text of the note associated with a command link button.</span></span> <span data-ttu-id="cdaed-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**кнопки \_ сетноте**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .</span><span class="sxs-lookup"><span data-stu-id="cdaed-107">You can send this message explicitly or use the [**Button\_SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cdaed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cdaed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdaed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cdaed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdaed-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cdaed-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cdaed-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cdaed-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cdaed-112">Указатель на строку типа **WCHAR** , заканчивающуюся нулем, которая содержит Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdaed-112">A pointer to a null-terminated **WCHAR** string that contains the note.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdaed-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cdaed-113">Return value</span></span>

<span data-ttu-id="cdaed-114">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cdaed-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdaed-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cdaed-115">Remarks</span></span>

<span data-ttu-id="cdaed-116">Начиная с Comctl32 DLL версии 6,01, кнопки ссылки на команды могут иметь Примечание.</span><span class="sxs-lookup"><span data-stu-id="cdaed-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span>

<span data-ttu-id="cdaed-117">Сообщение **BCM \_ сетноте** работает только с стилями кнопки [**BS \_ коммандлинк**](button-styles.md) и [**BS \_ дефкоммандлинк**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="cdaed-117">The **BCM\_SETNOTE** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdaed-118">Требования</span><span class="sxs-lookup"><span data-stu-id="cdaed-118">Requirements</span></span>



| <span data-ttu-id="cdaed-119">Требование</span><span class="sxs-lookup"><span data-stu-id="cdaed-119">Requirement</span></span> | <span data-ttu-id="cdaed-120">Значение</span><span class="sxs-lookup"><span data-stu-id="cdaed-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cdaed-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cdaed-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cdaed-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdaed-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cdaed-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cdaed-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cdaed-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cdaed-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cdaed-125">Header</span><span class="sxs-lookup"><span data-stu-id="cdaed-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdaed-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdaed-126"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdaed-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cdaed-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="cdaed-128">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="cdaed-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cdaed-129">Стили кнопок</span><span class="sxs-lookup"><span data-stu-id="cdaed-129">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="cdaed-130">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="cdaed-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cdaed-131">Типы кнопок</span><span class="sxs-lookup"><span data-stu-id="cdaed-131">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





