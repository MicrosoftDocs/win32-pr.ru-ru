---
description: Проверяет, может ли объект Инкдивидер использовать класс Инкрекогнизерконтекст для анализа слов.
ms.assetid: fd848fcc-5258-401f-8b51-b9d57da173da
title: Функция Рекогнизерконтекстсет
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizerContextSet
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 51e75b810c2103afed2e8ac8a28706b9c9af5da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910431"
---
# <a name="recognizercontextset-function"></a><span data-ttu-id="368f0-103">Функция Рекогнизерконтекстсет</span><span class="sxs-lookup"><span data-stu-id="368f0-103">RecognizerContextSet function</span></span>

<span data-ttu-id="368f0-104">Проверяет, может ли объект [**инкдивидер**](inkdivider-class.md) использовать класс [**инкрекогнизерконтекст**](inkrecognizercontext-class.md) для анализа слов.</span><span class="sxs-lookup"><span data-stu-id="368f0-104">Tests whether the [**InkDivider**](inkdivider-class.md) object can use the [**InkRecognizerContext**](inkrecognizercontext-class.md) class to analyze words.</span></span>

<span data-ttu-id="368f0-105">Эта функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="368f0-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="368f0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="368f0-106">Syntax</span></span>


```C++
HRESULT WINAPI RecognizerContextSet(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="368f0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="368f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="368f0-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="368f0-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="368f0-109">Маркер объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="368f0-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="368f0-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="368f0-110">Return value</span></span>

<span data-ttu-id="368f0-111">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="368f0-111">This function can return one of these values.</span></span>



| <span data-ttu-id="368f0-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="368f0-112">Return code</span></span>                                                                                  | <span data-ttu-id="368f0-113">Описание</span><span class="sxs-lookup"><span data-stu-id="368f0-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="368f0-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="368f0-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="368f0-115">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="368f0-115">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="368f0-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="368f0-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="368f0-117">Недопустимый параметр *пдивидер* .</span><span class="sxs-lookup"><span data-stu-id="368f0-117">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="368f0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="368f0-118">Requirements</span></span>



| <span data-ttu-id="368f0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="368f0-119">Requirement</span></span> | <span data-ttu-id="368f0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="368f0-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="368f0-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="368f0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="368f0-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="368f0-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="368f0-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="368f0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="368f0-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="368f0-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="368f0-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="368f0-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="368f0-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="368f0-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




