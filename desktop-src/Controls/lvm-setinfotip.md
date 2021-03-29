---
title: Сообщение LVM_SETINFOTIP (Коммктрл. h)
description: Задает текст подсказки в отложенном ответе на \_ уведомление ЛВН жетинфотип.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- Элементы управления Windows для LVM_SETINFOTIP сообщений
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654421"
---
# <a name="lvm_setinfotip-message"></a><span data-ttu-id="274ce-104">\_Сообщение LVM сетинфотип</span><span class="sxs-lookup"><span data-stu-id="274ce-104">LVM\_SETINFOTIP message</span></span>

<span data-ttu-id="274ce-105">Задает текст подсказки в отложенном ответе на уведомление [ЛВН \_ жетинфотип](lvn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="274ce-105">Sets tooltip text in delayed response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification.</span></span>

## <a name="parameters"></a><span data-ttu-id="274ce-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="274ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="274ce-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="274ce-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="274ce-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="274ce-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="274ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="274ce-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="274ce-110">Указатель на структуру <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">лвсетинфотип</a> , содержащую сведения, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="274ce-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="274ce-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="274ce-111">Return value</span></span>

<span data-ttu-id="274ce-112">Возвращает **значение true** , если текст подсказки установлен успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="274ce-112">Returns **TRUE** if the tooltip text is set successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="274ce-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="274ce-113">Remarks</span></span>

<span data-ttu-id="274ce-114">Сообщение **LVM \_ сетинфотип** позволяет приложению вычислить инфотипс в фоновом режиме, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="274ce-114">The **LVM\_SETINFOTIP** message lets an application calculate infotips in the background by performing the following steps:</span></span>

1.  <span data-ttu-id="274ce-115">В ответ на уведомление [ЛВН \_ жетинфотип](lvn-getinfotip.md) установите в качестве элемента **псзтекст** структуры [**нмлвжетинфотип**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) пустую строку и возвратите 0.</span><span class="sxs-lookup"><span data-stu-id="274ce-115">In response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification, set the **pszText** member of the [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure to an empty string and return 0.</span></span>
2.  <span data-ttu-id="274ce-116">В фоновом режиме Вычислите всплывающую подсказку.</span><span class="sxs-lookup"><span data-stu-id="274ce-116">In the background, compute the infotip.</span></span>
3.  <span data-ttu-id="274ce-117">После вычисления подсказки отправьте сообщение **LVM \_ сетинфотип** , установив элемент **псзтекст** структуры [**лвсетинфотип**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) в подсказку, а элементы **Член iItem** и **iSubItem** — к элементу и подэлементу, к которому применяется подсказка.</span><span class="sxs-lookup"><span data-stu-id="274ce-117">After computing the infotip, send the **LVM\_SETINFOTIP** message, setting the **pszText** member of the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure to the infotip and the **iItem** and **iSubItem** members to the item and sub-item to which the infotip applies.</span></span>

<span data-ttu-id="274ce-118">Текст, передаваемый в сообщение **LVM \_ сетинфотип** , отображается только в том случае, если элемент и подэлемент, описываемые структурой [**лвсетинфотип**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) , по-прежнему находятся в состоянии, требующем подсказки.</span><span class="sxs-lookup"><span data-stu-id="274ce-118">The text passed to the **LVM\_SETINFOTIP** message appears only if the item and sub-item described by the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure are still in a state that requires an infotip</span></span>

> [!Note]  
> <span data-ttu-id="274ce-119">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="274ce-119">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="274ce-120">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="274ce-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="274ce-121">Требования</span><span class="sxs-lookup"><span data-stu-id="274ce-121">Requirements</span></span>



| <span data-ttu-id="274ce-122">Требование</span><span class="sxs-lookup"><span data-stu-id="274ce-122">Requirement</span></span> | <span data-ttu-id="274ce-123">Значение</span><span class="sxs-lookup"><span data-stu-id="274ce-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="274ce-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="274ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="274ce-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="274ce-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="274ce-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="274ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="274ce-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="274ce-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="274ce-128">Header</span><span class="sxs-lookup"><span data-stu-id="274ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="274ce-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="274ce-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





