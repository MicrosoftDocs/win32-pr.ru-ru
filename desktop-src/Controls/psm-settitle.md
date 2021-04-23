---
title: Сообщение PSM_SETTITLE (Пршт. h)
description: Задает заголовок страницы свойств. Это сообщение можно отправить явным образом или с помощью \_ макроса пропшит сеттитле.
ms.assetid: 53ce8e20-4554-41f4-bad9-fb24c2c93c34
keywords:
- Элементы управления Windows для PSM_SETTITLE сообщений
topic_type:
- apiref
api_name:
- PSM_SETTITLE
- PSM_SETTITLEA
- PSM_SETTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a848a5bdaeaae64b6f1825740d1e8ade07a5a22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988234"
---
# <a name="psm_settitle-message"></a><span data-ttu-id="b5eec-105">\_Сообщение ПСМ сеттитле</span><span class="sxs-lookup"><span data-stu-id="b5eec-105">PSM\_SETTITLE message</span></span>

<span data-ttu-id="b5eec-106">Задает заголовок страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="b5eec-106">Sets the title of a property sheet.</span></span> <span data-ttu-id="b5eec-107">Это сообщение можно отправить явным образом или с помощью макроса [**пропшит \_ сеттитле**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) .</span><span class="sxs-lookup"><span data-stu-id="b5eec-107">You can send this message explicitly or by using the [**PropSheet\_SetTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_settitle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b5eec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b5eec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5eec-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5eec-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5eec-110">Флаг, указывающий, включать ли префикс "Свойства" или суффикс "Properties" (в зависимости от версии) с указанной строкой заголовка.</span><span class="sxs-lookup"><span data-stu-id="b5eec-110">Flag that indicates whether to include the prefix "Properties for" or the suffix "Properties" (depending on the version) with the specified title string.</span></span> <span data-ttu-id="b5eec-111">Если это значение равно КОМАНДНОМ PSH \_ проптитле, то добавляется префикс или суффикс.</span><span class="sxs-lookup"><span data-stu-id="b5eec-111">If this value is PSH\_PROPTITLE, the prefix or suffix is included.</span></span>

</dd> <dt>

<span data-ttu-id="b5eec-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5eec-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5eec-113">Указатель на буфер, содержащий строку заголовка.</span><span class="sxs-lookup"><span data-stu-id="b5eec-113">Pointer to a buffer that contains the title string.</span></span> <span data-ttu-id="b5eec-114">Если [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) этого параметра имеет **значение NULL**, то страница свойств загружает строковый ресурс, указанный в параметре [**ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5eec-114">If the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this parameter is **NULL**, the property sheet loads the string resource specified in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5eec-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b5eec-115">Return value</span></span>

<span data-ttu-id="b5eec-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="b5eec-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5eec-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5eec-117">Remarks</span></span>

<span data-ttu-id="b5eec-118">В мастере Aero это сообщение можно использовать для динамического изменения заголовка внутренней страницы. Например, при обработке уведомления [PSN \_ сетактиве](psn-setactive.md) .</span><span class="sxs-lookup"><span data-stu-id="b5eec-118">In an Aero Wizard, this message can be used to change the title of an interior page dynamically; for example, when handling the [PSN\_SETACTIVE](psn-setactive.md) notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5eec-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b5eec-119">Requirements</span></span>



| <span data-ttu-id="b5eec-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b5eec-120">Requirement</span></span> | <span data-ttu-id="b5eec-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b5eec-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5eec-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5eec-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b5eec-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5eec-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b5eec-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5eec-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b5eec-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5eec-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5eec-126">Header</span><span class="sxs-lookup"><span data-stu-id="b5eec-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5eec-127"><dt>Пршт. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5eec-127"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="b5eec-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b5eec-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b5eec-129">**ПСМ \_ СЕТТИТЛЕВ** (Юникод) и **ПСМ \_ сеттитлеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b5eec-129">**PSM\_SETTITLEW** (Unicode) and **PSM\_SETTITLEA** (ANSI)</span></span><br/>              |



 

