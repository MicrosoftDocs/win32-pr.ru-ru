---
description: Извлекает данные анализа из объекта Инкдивидер.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: Функция Каллдивиде
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539455"
---
# <a name="calldivide-function"></a><span data-ttu-id="81de1-103">Функция Каллдивиде</span><span class="sxs-lookup"><span data-stu-id="81de1-103">CallDivide function</span></span>

<span data-ttu-id="81de1-104">Извлекает данные анализа из объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81de1-104">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="81de1-105">Эта функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="81de1-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="81de1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81de1-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a><span data-ttu-id="81de1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="81de1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81de1-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81de1-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-109">Маркер объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81de1-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="81de1-110">*пвордсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81de1-110">*pWordSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-111">Размер слова, возвращаемого объектом [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81de1-111">The size of the word returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="81de1-112">*плинесизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81de1-112">*pLineSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-113">Размер строки, возвращаемой объектом [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81de1-113">The size of the line returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="81de1-114">*ппараграфсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81de1-114">*pParagraphSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-115">Размер абзаца, возвращаемого объектом [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81de1-115">The size of the paragraph returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="81de1-116">*пдравингсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="81de1-116">*pDrawingSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-117">Размер рисунка, возвращаемого объектом [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="81de1-117">The size of the drawing returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="81de1-118">*пвордкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81de1-118">*pWordCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-119">Количество слов, возвращаемых функцией анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="81de1-119">The number of words returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="81de1-120">*плинекаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81de1-120">*pLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-121">Число строк, возвращенных функцией анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="81de1-121">The number of lines returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="81de1-122">*ппараграфкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="81de1-122">*pParagraphCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="81de1-123">Число абзацев, возвращаемых функцией анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="81de1-123">The number of paragraphs returned by ink analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81de1-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="81de1-124">Return value</span></span>

<span data-ttu-id="81de1-125">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="81de1-125">This function can return one of these values.</span></span>



| <span data-ttu-id="81de1-126">Код возврата</span><span class="sxs-lookup"><span data-stu-id="81de1-126">Return code</span></span>                                                                                  | <span data-ttu-id="81de1-127">Описание</span><span class="sxs-lookup"><span data-stu-id="81de1-127">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="81de1-128"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="81de1-128"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="81de1-129">Функция выполнено.</span><span class="sxs-lookup"><span data-stu-id="81de1-129">The function suceeded.</span></span><br/>              |
| <dl> <span data-ttu-id="81de1-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="81de1-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="81de1-131">Один или несколько параметров недопустимы.</span><span class="sxs-lookup"><span data-stu-id="81de1-131">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81de1-132">Требования</span><span class="sxs-lookup"><span data-stu-id="81de1-132">Requirements</span></span>



| <span data-ttu-id="81de1-133">Требование</span><span class="sxs-lookup"><span data-stu-id="81de1-133">Requirement</span></span> | <span data-ttu-id="81de1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="81de1-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81de1-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81de1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="81de1-136">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="81de1-136">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="81de1-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81de1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="81de1-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="81de1-138">None supported</span></span><br/>                                                             |
| <span data-ttu-id="81de1-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="81de1-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="81de1-140"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81de1-140"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




