---
description: Удаляет объект Инкдивидер и освобождает связанные ресурсы.
ms.assetid: adf772e0-2829-4410-83c4-45a24bf3a848
title: Функция Делетеинкдивидер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteInkDivider
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 8338d179b0bd57232463c794feca96885ee006fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912352"
---
# <a name="deleteinkdivider-function"></a><span data-ttu-id="e3228-103">Функция Делетеинкдивидер</span><span class="sxs-lookup"><span data-stu-id="e3228-103">DeleteInkDivider function</span></span>

<span data-ttu-id="e3228-104">Удаляет объект [**инкдивидер**](inkdivider-class.md) и освобождает связанные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="e3228-104">Deletes an [**InkDivider**](inkdivider-class.md) object and releases associated resources.</span></span>

<span data-ttu-id="e3228-105">Эта функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="e3228-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3228-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3228-106">Syntax</span></span>


```C++
HRESULT WINAPI DeleteInkDivider(
  _In_ INT_PTR hDivider
);
```



## <a name="parameters"></a><span data-ttu-id="e3228-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3228-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3228-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3228-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3228-109">Маркер объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e3228-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3228-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3228-110">Return value</span></span>

<span data-ttu-id="e3228-111">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e3228-111">This function can return one of these values.</span></span>



| <span data-ttu-id="e3228-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e3228-112">Return code</span></span>                                                                                  | <span data-ttu-id="e3228-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e3228-113">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="e3228-114"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e3228-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e3228-115">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="e3228-115">The method succeeded.</span></span><br/>                |
| <dl> <span data-ttu-id="e3228-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e3228-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e3228-117">Недопустимый параметр *хдивидер* .</span><span class="sxs-lookup"><span data-stu-id="e3228-117">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e3228-118">Требования</span><span class="sxs-lookup"><span data-stu-id="e3228-118">Requirements</span></span>



| <span data-ttu-id="e3228-119">Требование</span><span class="sxs-lookup"><span data-stu-id="e3228-119">Requirement</span></span> | <span data-ttu-id="e3228-120">Значение</span><span class="sxs-lookup"><span data-stu-id="e3228-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3228-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3228-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e3228-122">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="e3228-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e3228-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3228-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e3228-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e3228-124">None supported</span></span><br/>                                                             |
| <span data-ttu-id="e3228-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3228-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3228-126"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3228-126"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




