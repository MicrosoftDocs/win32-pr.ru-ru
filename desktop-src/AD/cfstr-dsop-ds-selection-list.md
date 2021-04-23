---
title: CFSTR_DSOP_DS_SELECTION_LIST (Обжсел. h)
description: '\_ \_ \_ \_ Формат буфера обмена списка выбора КФСТР ДСОП DS предоставляет хглобал, который содержит \_ \_ структуру списка выбора DS. \_ \_ Структура списка выбора DS содержит данные о элементах, выбранных в диалоговом окне Выбор объектов каталога.'
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988494"
---
# <a name="cfstr_dsop_ds_selection_list"></a><span data-ttu-id="804cb-104">\_ \_ \_ список выбора кфстр ДСОП \_ DS</span><span class="sxs-lookup"><span data-stu-id="804cb-104">CFSTR\_DSOP\_DS\_SELECTION\_LIST</span></span>

<dl> <dt>

<span data-ttu-id="804cb-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**\_ \_ \_ список выбора кфстр ДСОП \_ DS**</span><span class="sxs-lookup"><span data-stu-id="804cb-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR\_DSOP\_DS\_SELECTION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="804cb-106">" \_ \_ список выбора кфстр ДСОП DS \_ \_ "</span><span class="sxs-lookup"><span data-stu-id="804cb-106">"CFSTR\_DSOP\_DS\_SELECTION\_LIST"</span></span>
</dt> <dt>



<span data-ttu-id="804cb-107">Формат буфера обмена **\_ \_ \_ \_ списка выбора кфстр ДСОП DS** предоставляется с помощью интерфейса [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) , полученного путем вызова [**идсобжектпиккер:: инвокедиалог**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span><span class="sxs-lookup"><span data-stu-id="804cb-107">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format is provided by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtained by calling [**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span></span> <span data-ttu-id="804cb-108">Формат буфера обмена **\_ \_ \_ \_ списка выбора кфстр ДСОП DS** предоставляет **Хглобал** , который содержит структуру [**\_ \_ списка выбора DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) .</span><span class="sxs-lookup"><span data-stu-id="804cb-108">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format provides an **HGLOBAL** that contains a [**DS\_SELECTION\_LIST**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) structure.</span></span> <span data-ttu-id="804cb-109">Структура **\_ \_ списка выбора DS** содержит данные о элементах, выбранных в диалоговом окне [Выбор объектов каталога](directory-object-picker.md) .</span><span class="sxs-lookup"><span data-stu-id="804cb-109">The **DS\_SELECTION\_LIST** structure contains data about the items selected in a [Directory Object Picker](directory-object-picker.md) dialog box.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="804cb-110">Требования</span><span class="sxs-lookup"><span data-stu-id="804cb-110">Requirements</span></span>



| <span data-ttu-id="804cb-111">Требование</span><span class="sxs-lookup"><span data-stu-id="804cb-111">Requirement</span></span> | <span data-ttu-id="804cb-112">Значение</span><span class="sxs-lookup"><span data-stu-id="804cb-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="804cb-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="804cb-113">Minimum supported client</span></span><br/> | <span data-ttu-id="804cb-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="804cb-114">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="804cb-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="804cb-115">Minimum supported server</span></span><br/> | <span data-ttu-id="804cb-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="804cb-116">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="804cb-117">Header</span><span class="sxs-lookup"><span data-stu-id="804cb-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="804cb-118"><dt>Обжсел. h</dt></span><span class="sxs-lookup"><span data-stu-id="804cb-118"><dt>Objsel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="804cb-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="804cb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="804cb-120">**\_список выбора \_ DS**</span><span class="sxs-lookup"><span data-stu-id="804cb-120">**DS\_SELECTION\_LIST**</span></span>](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[<span data-ttu-id="804cb-121">**Идсобжектпиккер:: Инвокедиалог**</span><span class="sxs-lookup"><span data-stu-id="804cb-121">**IDsObjectPicker::InvokeDialog**</span></span>](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[<span data-ttu-id="804cb-122">Средство выбора объектов каталога</span><span class="sxs-lookup"><span data-stu-id="804cb-122">Directory Object Picker</span></span>](directory-object-picker.md)
</dt> </dl>

 

