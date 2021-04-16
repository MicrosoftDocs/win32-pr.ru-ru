---
description: Задает свойство LineHeight объекта Инкдивидер.
ms.assetid: ce5e40c5-faa1-4d66-94f4-d5bd1a11ee4c
title: Функция Сетлинехеигхт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetLineHeight
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: be4045e01ac890471536d95768668b633d8f2249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712356"
---
# <a name="setlineheight-function"></a><span data-ttu-id="23d12-103">Функция Сетлинехеигхт</span><span class="sxs-lookup"><span data-stu-id="23d12-103">SetLineHeight function</span></span>

<span data-ttu-id="23d12-104">Задает свойство [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="23d12-104">Sets the [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property on the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="23d12-105">Эта вспомогательная функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="23d12-105">This helper function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="23d12-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23d12-106">Syntax</span></span>


```C++
HRESULT WINAPI SetLineHeight(
  _In_ INT_PTR hDivider,
  _In_ LONG    lLineHeight
);
```



## <a name="parameters"></a><span data-ttu-id="23d12-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="23d12-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23d12-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23d12-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d12-109">Маркер объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="23d12-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="23d12-110">*ллинехеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23d12-110">*lLineHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23d12-111">Свойство [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) объекта [**инкдивидер**](inkdivider-class.md) в единицах HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="23d12-111">The [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight) property of the [**InkDivider**](inkdivider-class.md) object, in HIMETRIC units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23d12-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23d12-112">Return value</span></span>

<span data-ttu-id="23d12-113">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="23d12-113">This function can return one of these values.</span></span>



| <span data-ttu-id="23d12-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="23d12-114">Return code</span></span>                                                                                  | <span data-ttu-id="23d12-115">Описание</span><span class="sxs-lookup"><span data-stu-id="23d12-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="23d12-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="23d12-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="23d12-117">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="23d12-117">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="23d12-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="23d12-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="23d12-119">Недопустимый параметр *пдивидер* .</span><span class="sxs-lookup"><span data-stu-id="23d12-119">The *pDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="23d12-120">Требования</span><span class="sxs-lookup"><span data-stu-id="23d12-120">Requirements</span></span>



| <span data-ttu-id="23d12-121">Требование</span><span class="sxs-lookup"><span data-stu-id="23d12-121">Requirement</span></span> | <span data-ttu-id="23d12-122">Значение</span><span class="sxs-lookup"><span data-stu-id="23d12-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23d12-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23d12-123">Minimum supported client</span></span><br/> | <span data-ttu-id="23d12-124">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="23d12-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="23d12-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23d12-125">Minimum supported server</span></span><br/> | <span data-ttu-id="23d12-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="23d12-126">None supported</span></span><br/>                                                             |
| <span data-ttu-id="23d12-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23d12-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="23d12-128"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23d12-128"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 
