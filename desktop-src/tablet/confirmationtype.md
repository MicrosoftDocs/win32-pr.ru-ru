---
description: Указывает тип подтверждения, которое может произойти для объекта Иконтекстноде.
ms.assetid: 5c906548-dbf5-4448-b248-070bd43b054e
title: Перечисление Конфирматионтипе (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfirmationType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 2c43971c6ccf44513c11e46d4bc5db86d973d7f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710866"
---
# <a name="confirmationtype-enumeration"></a><span data-ttu-id="3a2a0-103">Перечисление Конфирматионтипе</span><span class="sxs-lookup"><span data-stu-id="3a2a0-103">ConfirmationType enumeration</span></span>

<span data-ttu-id="3a2a0-104">Указывает тип подтверждения, которое может произойти для объекта [**иконтекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="3a2a0-104">Specifies the type of confirmation that can occur on an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2a0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a2a0-105">Syntax</span></span>


```C++
typedef enum ConfirmationType { 
  ConfirmationType_None                   = 0,
  ConfirmationType_NodeTypeAndProperties  = 1,
  ConfirmationType_TopBoundary            = 4
} ConfirmationType;
```



## <a name="constants"></a><span data-ttu-id="3a2a0-106">Константы</span><span class="sxs-lookup"><span data-stu-id="3a2a0-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3a2a0-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**Конфирматионтипе \_ None**</span><span class="sxs-lookup"><span data-stu-id="3a2a0-107"><span id="ConfirmationType_None"></span><span id="confirmationtype_none"></span><span id="CONFIRMATIONTYPE_NONE"></span>**ConfirmationType\_None**</span></span>
</dt> <dd>

<span data-ttu-id="3a2a0-108">Подтверждение не применяется.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-108">No confirmation is applied.</span></span> <span data-ttu-id="3a2a0-109">[**Иинканализер**](iinkanalyzer.md) может свободно изменять контекстный узел или любой из его потомков по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-109">The [**IInkAnalyzer**](iinkanalyzer.md) is free to change a context node or any of its descendants as needed.</span></span>

</dd> <dt>

<span data-ttu-id="3a2a0-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**Конфирматионтипе \_ нодетипеандпропертиес**</span><span class="sxs-lookup"><span data-stu-id="3a2a0-110"><span id="ConfirmationType_NodeTypeAndProperties"></span><span id="confirmationtype_nodetypeandproperties"></span><span id="CONFIRMATIONTYPE_NODETYPEANDPROPERTIES"></span>**ConfirmationType\_NodeTypeAndProperties**</span></span>
</dt> <dd>

<span data-ttu-id="3a2a0-111">[**Иинканализер**](iinkanalyzer.md) не может изменить тип или любые свойства указанного контекстного узла.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-111">The [**IInkAnalyzer**](iinkanalyzer.md) cannot change the type or any properties of the specified context node.</span></span>

</dd> <dt>

<span data-ttu-id="3a2a0-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**Конфирматионтипе \_ топбаундари**</span><span class="sxs-lookup"><span data-stu-id="3a2a0-112"><span id="ConfirmationType_TopBoundary"></span><span id="confirmationtype_topboundary"></span><span id="CONFIRMATIONTYPE_TOPBOUNDARY"></span>**ConfirmationType\_TopBoundary**</span></span>
</dt> <dd>

<span data-ttu-id="3a2a0-113">[**Иинканализер**](iinkanalyzer.md) не будет выполнять операции, включая добавление рукописного ввода или слияния с другими [**контекстнодес**](icontextnodes.md), которые приводят к перемещению топбаундари за пределы текущей верхней границы.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-113">The [**IInkAnalyzer**](iinkanalyzer.md) will not perform operations, including adding ink or merging with other [**ContextNodes**](icontextnodes.md), that cause the TopBoundary to move beyond the current top boundary.</span></span> <span data-ttu-id="3a2a0-114">Пример:</span><span class="sxs-lookup"><span data-stu-id="3a2a0-114">For example:</span></span>

-   <span data-ttu-id="3a2a0-115">Приложение анализирует набор рукописных данных, и идентифицируется Параграфноде.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-115">An application analyzes a set of Ink, and a ParagraphNode is identified.</span></span>
-   <span data-ttu-id="3a2a0-116">Приложение подтверждает Топбаундари этого абзаца.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-116">The application confirms the TopBoundary of this paragraph.</span></span>
-   <span data-ttu-id="3a2a0-117">Пользователь приложения записывает новые рукописные данные над текущим абзацем.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-117">The user of the application writes new ink above the current paragraph.</span></span> <span data-ttu-id="3a2a0-118">При повторном вызове анализа новые рукописные данные не будут включены в узел подтвержденного абзаца.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-118">When analyze is called again, the new ink will not be incorporated into the Confirmed paragraph node.</span></span>
-   <span data-ttu-id="3a2a0-119">Так как подтверждена только верхняя граница, Контекстноде может продолжать расти в других направлениях.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-119">Since only the top boundary is confirmed, the ContextNode can continue to grow in other directions.</span></span> <span data-ttu-id="3a2a0-120">Удаление штрихов может привести к перемещению верхней границы.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-120">Deleting strokes can cause the top boundary to move down.</span></span> <span data-ttu-id="3a2a0-121">Преобразование Контекстноде может привести к изменению расположения, но не позволит объединить дополнительные рукописные данные в новом месте.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-121">Translating the ContextNode can cause the location to change, but will not allow additional ink to be merged in the new location.</span></span>

<span data-ttu-id="3a2a0-122">Этот Конфирматионтипе применим только к узлам абзаца.</span><span class="sxs-lookup"><span data-stu-id="3a2a0-122">This ConfirmationType is only applicable to paragraph nodes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a2a0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a2a0-123">Remarks</span></span>

<span data-ttu-id="3a2a0-124">Значение **нодетипеандпропертиес** можно использовать только для узлов рукописного ввода и вывода рукописного текста (см. раздел [**Иконтекстноде:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="3a2a0-124">You can use the **NodeTypeAndProperties** value only for ink word and ink drawing nodes (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="3a2a0-125">В противном случае возвращается **E \_ INVALIDARG** из [**иконтекстноде:: Confirm**](icontextnode-confirm.md).</span><span class="sxs-lookup"><span data-stu-id="3a2a0-125">Otherwise, an **E\_INVALIDARG** is returned from [**IContextNode::Confirm**](icontextnode-confirm.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2a0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="3a2a0-126">Requirements</span></span>



| <span data-ttu-id="3a2a0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="3a2a0-127">Requirement</span></span> | <span data-ttu-id="3a2a0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="3a2a0-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2a0-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a2a0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3a2a0-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3a2a0-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3a2a0-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a2a0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3a2a0-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3a2a0-132">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3a2a0-133">Header</span><span class="sxs-lookup"><span data-stu-id="3a2a0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a2a0-134"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3a2a0-134"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2a0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a2a0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2a0-136">**Иконтекстноде:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="3a2a0-136">**IContextNode::Confirm**</span></span>](icontextnode-confirm.md)
</dt> <dt>

[<span data-ttu-id="3a2a0-137">**Иконтекстноде:: Confirm**</span><span class="sxs-lookup"><span data-stu-id="3a2a0-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> </dl>

 

 




