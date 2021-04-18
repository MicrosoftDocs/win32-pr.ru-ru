---
description: Извлекает результаты анализа из объекта Инкдивидер.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: Функция Каллдивидересултс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143006"
---
# <a name="calldivideresults-function"></a><span data-ttu-id="af6fd-103">Функция Каллдивидересултс</span><span class="sxs-lookup"><span data-stu-id="af6fd-103">CallDivideResults function</span></span>

<span data-ttu-id="af6fd-104">Извлекает результаты анализа из объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="af6fd-104">Retrieves analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="af6fd-105">Эта функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="af6fd-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="af6fd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af6fd-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a><span data-ttu-id="af6fd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="af6fd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af6fd-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-109">Маркер объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="af6fd-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-110">*авордстрокеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-110">*aWordStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-111">Массив идентификаторов, связанный со словом, которое передается в класс [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="af6fd-111">An array of identifiers associated with the word that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-112">*алинестрокеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-112">*aLineStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-113">Массив свойств [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , связанных со строкой, передаваемой в класс [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="af6fd-113">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the line that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-114">*апараграфстрокеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-114">*aParagraphStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-115">Массив свойств [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , связанных с абзацем из класса [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="af6fd-115">An array of the [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the paragraph from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-116">*адравингстрокеидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-116">*aDrawingStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-117">Массив свойств [**идентификатора**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) для объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , связанных с рисованием из класса [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="af6fd-117">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the drawing from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-118">*пастрвордс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-118">*pastrWords* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-119">Массив слов, возвращаемых из анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="af6fd-119">An array of words returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-120">*пастрлинес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-120">*pastrLines* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-121">Массив строк, возвращенных из анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="af6fd-121">An array of lines returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-122">*пастрпараграфс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-122">*pastrParagraphs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-123">Массив абзацев, возвращенных из анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="af6fd-123">An array of paragraphs returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-124">*авордротатионцентеркс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-124">*aWordRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-125">Массив центральных точек слов вдоль оси x из анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="af6fd-125">An array of the center points of the words along the x-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-126">*авордротатионцентери* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-126">*aWordRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-127">Массив центральных точек слов вдоль оси y из анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="af6fd-127">An array of the center points of the words along the y-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-128">*авордангле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-128">*aWordAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-129">Массив, содержащий углы, на которые поворачиваются слова для получения лучших результатов анализа.</span><span class="sxs-lookup"><span data-stu-id="af6fd-129">An array containing the angles by which to rotate the words for best analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-130">*алинеротатионцентеркс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-130">*aLineRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-131">Массив, содержащий центральные точки линий вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="af6fd-131">An array containing the center points of the lines along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-132">*алинеротатионцентери* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-132">*aLineRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-133">Массив, содержащий центральные точки линий вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="af6fd-133">An array containing the center points of the lines along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="af6fd-134">*алинеангле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-134">*aLineAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af6fd-135">Массив, содержащий углы, на которые поворачиваются линии для получения наилучших результатов анализа.</span><span class="sxs-lookup"><span data-stu-id="af6fd-135">An array containing the angles by which to rotate the lines for best analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af6fd-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af6fd-136">Return value</span></span>

<span data-ttu-id="af6fd-137">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="af6fd-137">This function can return one of these values.</span></span>



| <span data-ttu-id="af6fd-138">Код возврата</span><span class="sxs-lookup"><span data-stu-id="af6fd-138">Return code</span></span>                                                                                   | <span data-ttu-id="af6fd-139">Описание</span><span class="sxs-lookup"><span data-stu-id="af6fd-139">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="af6fd-140"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="af6fd-140"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="af6fd-141">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="af6fd-141">The function succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="af6fd-142"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="af6fd-142"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="af6fd-143">Недопустимый параметр *хдивидер* .</span><span class="sxs-lookup"><span data-stu-id="af6fd-143">The *hDivider* parameter is invalid.</span></span><br/>                   |
| <dl> <span data-ttu-id="af6fd-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="af6fd-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="af6fd-145">Не удалось выделить достаточно памяти для хранения результатов.</span><span class="sxs-lookup"><span data-stu-id="af6fd-145">Could not allocate enough memory to store the results.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="af6fd-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af6fd-146">Remarks</span></span>

<span data-ttu-id="af6fd-147">Чтобы избежать утечек памяти, необходимо освободить ресурсы для *пастрвордс*, *пастрлинес* и *пастрпараграфс*.</span><span class="sxs-lookup"><span data-stu-id="af6fd-147">To avoid memory leaks you must release the resources for *pastrWords*, *pastrLines*, and *pastrParagraphs*.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6fd-148">Требования</span><span class="sxs-lookup"><span data-stu-id="af6fd-148">Requirements</span></span>



| <span data-ttu-id="af6fd-149">Требование</span><span class="sxs-lookup"><span data-stu-id="af6fd-149">Requirement</span></span> | <span data-ttu-id="af6fd-150">Значение</span><span class="sxs-lookup"><span data-stu-id="af6fd-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af6fd-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af6fd-151">Minimum supported client</span></span><br/> | <span data-ttu-id="af6fd-152">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="af6fd-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="af6fd-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af6fd-153">Minimum supported server</span></span><br/> | <span data-ttu-id="af6fd-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="af6fd-154">None supported</span></span><br/>                                                             |
| <span data-ttu-id="af6fd-155">Библиотека</span><span class="sxs-lookup"><span data-stu-id="af6fd-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="af6fd-156"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af6fd-156"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




