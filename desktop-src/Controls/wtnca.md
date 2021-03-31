---
title: Значения ВТНКА (Укссеме. h)
description: Задает флаги для изменения атрибутов визуального стиля окна. Используйте одно или побитовое сочетание следующих значений.
ms.assetid: C71D1957-6572-4242-B715-C54BDFBBD6B7
topic_type:
- apiref
api_name:
- WTNCA_NODRAWCAPTION
- WTNCA_NODRAWICON
- WTNCA_NOSYSMENU
- WTNCA_NOMIRRORHELP
- WTNCA_VALIDBITS
api_location:
- Uxtheme.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaf543b688d0b403962da43029ac9aa85422bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137406"
---
# <a name="wtnca-values"></a><span data-ttu-id="098e4-104">Значения ВТНКА</span><span class="sxs-lookup"><span data-stu-id="098e4-104">WTNCA Values</span></span>

<span data-ttu-id="098e4-105">Задает флаги для изменения атрибутов визуального стиля окна.</span><span class="sxs-lookup"><span data-stu-id="098e4-105">Specifies flags that modify window visual style attributes.</span></span> <span data-ttu-id="098e4-106">Используйте одно или побитовое сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="098e4-106">Use one, or a bitwise combination of the following values.</span></span>



| <span data-ttu-id="098e4-107">Константа/значение</span><span class="sxs-lookup"><span data-stu-id="098e4-107">Constant/value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="098e4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="098e4-108">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="WTNCA_NODRAWCAPTION"></span><span id="wtnca_nodrawcaption"></span><dl> <span data-ttu-id="098e4-109"><dt>**Втнка \_ НОДРАВКАПТИОН**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="098e4-109"><dt>**WTNCA\_NODRAWCAPTION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="098e4-110">Предотвращает прорисовку заголовка окна.</span><span class="sxs-lookup"><span data-stu-id="098e4-110">Prevents the window caption from being drawn.</span></span><br/>                                |
| <span id="WTNCA_NODRAWICON"></span><span id="wtnca_nodrawicon"></span><dl> <span data-ttu-id="098e4-111"><dt>**Втнка \_ НОДРАВИКОН**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="098e4-111"><dt>**WTNCA\_NODRAWICON**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="098e4-112">Предотвращает прорисовку значка системы.</span><span class="sxs-lookup"><span data-stu-id="098e4-112">Prevents the system icon from being drawn.</span></span><br/>                                   |
| <span id="WTNCA_NOSYSMENU"></span><span id="wtnca_nosysmenu"></span><dl> <span data-ttu-id="098e4-113"><dt>**Втнка \_ НОСИСМЕНУ**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="098e4-113"><dt>**WTNCA\_NOSYSMENU**</dt> <dt>0x00000004</dt></span></span> </dl>             | <span data-ttu-id="098e4-114">Предотвращает появление в меню системного значка.</span><span class="sxs-lookup"><span data-stu-id="098e4-114">Prevents the system icon menu from appearing.</span></span><br/>                                |
| <span id="WTNCA_NOMIRRORHELP"></span><span id="wtnca_nomirrorhelp"></span><dl> <span data-ttu-id="098e4-115"><dt>**Втнка \_ НОМИРРОРХЕЛП**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="098e4-115"><dt>**WTNCA\_NOMIRRORHELP**</dt> <dt>0x00000008</dt></span></span> </dl>    | <span data-ttu-id="098e4-116">Предотвращает зеркальное отображение вопросительного знака даже в макете с направлением письма справа налево.</span><span class="sxs-lookup"><span data-stu-id="098e4-116">Prevents mirroring of the question mark, even in right-to-left (RTL) layout.</span></span><br/> |
| <span id="WTNCA_VALIDBITS"></span><span id="wtnca_validbits"></span><dl> <span data-ttu-id="098e4-117"><dt>**ВТНКА \_ валидбитс**</dt></span><span class="sxs-lookup"><span data-stu-id="098e4-117"><dt>**WTNCA\_VALIDBITS**</dt></span></span> </dl>                                                                             | <span data-ttu-id="098e4-118">Маска, которая содержит все допустимые биты.</span><span class="sxs-lookup"><span data-stu-id="098e4-118">A mask that contains all the valid bits.</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="098e4-119">Требования</span><span class="sxs-lookup"><span data-stu-id="098e4-119">Requirements</span></span>



| <span data-ttu-id="098e4-120">Требование</span><span class="sxs-lookup"><span data-stu-id="098e4-120">Requirement</span></span> | <span data-ttu-id="098e4-121">Значение</span><span class="sxs-lookup"><span data-stu-id="098e4-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="098e4-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="098e4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="098e4-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="098e4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="098e4-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="098e4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="098e4-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="098e4-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="098e4-126">Header</span><span class="sxs-lookup"><span data-stu-id="098e4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="098e4-127"><dt>Укссеме. h</dt></span><span class="sxs-lookup"><span data-stu-id="098e4-127"><dt>Uxtheme.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="098e4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="098e4-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="098e4-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="098e4-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="098e4-130">**\_Параметры ВТА**</span><span class="sxs-lookup"><span data-stu-id="098e4-130">**WTA\_OPTIONS**</span></span>](/windows/desktop/api/Uxtheme/ns-uxtheme-wta_options)
</dt> <dt>

[<span data-ttu-id="098e4-131">**сетвиндовсеменонклиентаттрибутес**</span><span class="sxs-lookup"><span data-stu-id="098e4-131">**SetWindowThemeNonClientAttributes**</span></span>](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowthemenonclientattributes)
</dt> </dl>

 

 





