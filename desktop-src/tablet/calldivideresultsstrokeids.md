---
description: Извлекает свойства идентификатора для объектов Иинкстрокедисп соответствующего слова, строки, абзаца или рисунка, определенных функцией анализа рукописного ввода.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: Функция Каллдивидересултсстрокеидс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701301"
---
# <a name="calldivideresultsstrokeids-function"></a><span data-ttu-id="7c7eb-103">Функция Каллдивидересултсстрокеидс</span><span class="sxs-lookup"><span data-stu-id="7c7eb-103">CallDivideResultsStrokeIds function</span></span>

<span data-ttu-id="7c7eb-104">Извлекает свойства [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) соответствующего слова, строки, абзаца или рисунка, определенных функцией анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-104">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span>

<span data-ttu-id="7c7eb-105">Эта функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7eb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c7eb-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a><span data-ttu-id="7c7eb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c7eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c7eb-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c7eb-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7eb-109">Маркер объекта- [разделителя](the-divider-object.md) .</span><span class="sxs-lookup"><span data-stu-id="7c7eb-109">A handle to the [Divider](the-divider-object.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="7c7eb-110">*\[ авордстрокеидс \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="7c7eb-110">*aWordStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7eb-111">Массив идентификаторов штрихов рукописного ввода в слове.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-111">An array of the stroke IDs of the ink in the word.</span></span>

</dd> <dt>

<span data-ttu-id="7c7eb-112">*\[ алинестрокеидс \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="7c7eb-112">*aLineStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7eb-113">Массив идентификаторов штриха для рукописного ввода в строке.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-113">An array of the stroke IDs of the ink in the line.</span></span>

</dd> <dt>

<span data-ttu-id="7c7eb-114">*\[ апараграфстрокеидс \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="7c7eb-114">*aParagraphStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7eb-115">Массив идентификаторов штрихов рукописного ввода в абзаце.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-115">An array of the stroke IDs of the ink in the paragraph.</span></span>

</dd> <dt>

<span data-ttu-id="7c7eb-116">*\[ адравингстрокеидс \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="7c7eb-116">*aDrawingStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7eb-117">Массив идентификаторов штрихов рукописного ввода в документе.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-117">An array of the stroke IDs of the ink in the drawing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c7eb-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c7eb-118">Return value</span></span>

<span data-ttu-id="7c7eb-119">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-119">This function can return one of these values.</span></span>



| <span data-ttu-id="7c7eb-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7c7eb-120">Return code</span></span>                                                                                  | <span data-ttu-id="7c7eb-121">Описание</span><span class="sxs-lookup"><span data-stu-id="7c7eb-121">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="7c7eb-122"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7c7eb-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7c7eb-123">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7c7eb-123">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="7c7eb-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7c7eb-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7c7eb-125">Недопустимый параметр *хдивидер* .</span><span class="sxs-lookup"><span data-stu-id="7c7eb-125">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c7eb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="7c7eb-126">Requirements</span></span>



| <span data-ttu-id="7c7eb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="7c7eb-127">Requirement</span></span> | <span data-ttu-id="7c7eb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="7c7eb-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c7eb-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c7eb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7c7eb-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7c7eb-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7c7eb-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c7eb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7c7eb-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7c7eb-132">None supported</span></span><br/>                                                             |
| <span data-ttu-id="7c7eb-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7c7eb-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c7eb-134"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c7eb-134"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




