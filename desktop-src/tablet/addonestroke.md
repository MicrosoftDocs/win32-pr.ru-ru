---
description: Добавляет новый объект Иинкстрокедисп в переданный объект Инкдивидер.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: Функция Аддонестроке
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496752"
---
# <a name="addonestroke-function"></a><span data-ttu-id="49e7e-103">Функция Аддонестроке</span><span class="sxs-lookup"><span data-stu-id="49e7e-103">AddOneStroke function</span></span>

<span data-ttu-id="49e7e-104">Добавляет новый объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) в переданный объект [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="49e7e-104">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>

<span data-ttu-id="49e7e-105">Эта функция не предназначена для использования в коде приложения.</span><span class="sxs-lookup"><span data-stu-id="49e7e-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="49e7e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49e7e-106">Syntax</span></span>


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a><span data-ttu-id="49e7e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="49e7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e7e-108">*хдивидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e7e-109">Маркер объекта [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="49e7e-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="49e7e-110">*строкеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-110">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e7e-111">[**Идентификатор**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , добавляемого в объект [**инкдивидер**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="49e7e-111">The [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to be added to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="49e7e-112">*cPoints* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-112">*cPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e7e-113">Число пакетов, составляющих новый объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="49e7e-113">The number of packets that make up the new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="49e7e-114">*апоинтс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-114">*aPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49e7e-115">Массив пакетов, составляющих объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) в *строкеид*.</span><span class="sxs-lookup"><span data-stu-id="49e7e-115">The array of packets that make up the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object in *strokeId*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e7e-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49e7e-116">Return value</span></span>

<span data-ttu-id="49e7e-117">Эта функция может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="49e7e-117">This function can return one of these values.</span></span>



| <span data-ttu-id="49e7e-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="49e7e-118">Return code</span></span>                                                                                  | <span data-ttu-id="49e7e-119">Описание</span><span class="sxs-lookup"><span data-stu-id="49e7e-119">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="49e7e-120"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="49e7e-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="49e7e-121">Функция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="49e7e-121">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="49e7e-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="49e7e-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="49e7e-123">Недопустимый параметр *хдивидер* .</span><span class="sxs-lookup"><span data-stu-id="49e7e-123">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="49e7e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="49e7e-124">Requirements</span></span>



| <span data-ttu-id="49e7e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="49e7e-125">Requirement</span></span> | <span data-ttu-id="49e7e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="49e7e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49e7e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49e7e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="49e7e-128">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="49e7e-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="49e7e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49e7e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="49e7e-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="49e7e-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="49e7e-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="49e7e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="49e7e-132"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49e7e-132"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




