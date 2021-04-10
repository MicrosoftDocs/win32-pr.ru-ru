---
title: Сообщение LVM_SETICONSPACING (Коммктрл. h)
description: Задает интервал между значками в элементах управления "представление списка", имеющим \_ стиль значка LVS. Это сообщение можно отправить явно или с помощью \_ макроса СетиконспаЦинг ListView.
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- Элементы управления Windows для LVM_SETICONSPACING сообщений
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891445"
---
# <a name="lvm_seticonspacing-message"></a><span data-ttu-id="8e9ef-105">\_Сообщение LVM сетиконспаЦинг</span><span class="sxs-lookup"><span data-stu-id="8e9ef-105">LVM\_SETICONSPACING message</span></span>

<span data-ttu-id="8e9ef-106">Задает интервал между значками в элементах управления "представление списка", имеющим стиль [**\_ значка LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8e9ef-106">Sets the spacing between icons in list-view controls that have the [**LVS\_ICON**](list-view-window-styles.md) style.</span></span> <span data-ttu-id="8e9ef-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сетиконспаЦинг ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) .</span><span class="sxs-lookup"><span data-stu-id="8e9ef-107">You can send this message explicitly or by using the [**ListView\_SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e9ef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e9ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e9ef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e9ef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e9ef-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e9ef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e9ef-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e9ef-112">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) задает расстояние (в пикселях), которое устанавливается между значками на оси x.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the distance, in pixels, to set between icons on the x-axis.</span></span> <span data-ttu-id="8e9ef-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) задает расстояние (в пикселях), которое устанавливается между значками на оси y.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the distance, in pixels, to set between icons on the y-axis.</span></span> <span data-ttu-id="8e9ef-114">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-114">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e9ef-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e9ef-115">Return value</span></span>

<span data-ttu-id="8e9ef-116">Возвращает значение **типа DWORD** , которое содержит предыдущее расстояние по оси x в нижнем слове и предыдущее расстояние по оси y в верхнем слове.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-116">Returns a **DWORD** value that contains the previous x-axis distance in the low word, and the previous y-axis distance in the high word.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e9ef-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e9ef-117">Remarks</span></span>

<span data-ttu-id="8e9ef-118">Значения для *lParam* задаются относительно левого верхнего угла точечного рисунка значка.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-118">Values for *lParam* are relative to the upper-left corner of an icon bitmap.</span></span> <span data-ttu-id="8e9ef-119">Таким образом, чтобы задать интервал между значками, которые не перекрываются, значения *lParam* должны включать размер значка, а также объем пустого пространства, необходимого между значками.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-119">Therefore, to set spacing between icons that do not overlap, the *lParam* values must include the size of the icon, plus the amount of empty space desired between icons.</span></span> <span data-ttu-id="8e9ef-120">Значения, которые не включают ширину значка, приводят к перекрытию.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-120">Values that do not include the width of the icon will result in overlaps.</span></span>

<span data-ttu-id="8e9ef-121">При определении расстояния между значками значения *lParam* должны иметь значение 4 или больше.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-121">When defining the icon spacing, the *lParam* values must set to 4 or larger.</span></span> <span data-ttu-id="8e9ef-122">Меньшие значения не будут давать желаемый макет.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-122">Smaller values will not yield the desired layout.</span></span> <span data-ttu-id="8e9ef-123">Чтобы сбросить значки по умолчанию, задайте значения *lParam* равными-1.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-123">To reset the icons to the default spacing, set the *lParam* values to -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e9ef-124">Требования</span><span class="sxs-lookup"><span data-stu-id="8e9ef-124">Requirements</span></span>



| <span data-ttu-id="8e9ef-125">Требование</span><span class="sxs-lookup"><span data-stu-id="8e9ef-125">Requirement</span></span> | <span data-ttu-id="8e9ef-126">Значение</span><span class="sxs-lookup"><span data-stu-id="8e9ef-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e9ef-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e9ef-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8e9ef-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e9ef-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e9ef-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e9ef-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8e9ef-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e9ef-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e9ef-131">Header</span><span class="sxs-lookup"><span data-stu-id="8e9ef-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e9ef-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e9ef-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

