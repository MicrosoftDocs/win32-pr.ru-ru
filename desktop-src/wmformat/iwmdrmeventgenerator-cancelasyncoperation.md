---
title: Метод Ивмдрмевентженератор Канцеласинкоператион (Вмдрмсдк. h)
description: Метод Канцеласинкоператион отменяет асинхронную операцию.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Формат Windows Media, Канцеласинкоператион метод
- Канцеласинкоператион метод Windows Media Format, интерфейс Ивмдрмевентженератор
- Интерфейс Ивмдрмевентженератор Windows Media Format, метод Канцеласинкоператион
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657373"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a><span data-ttu-id="a8a9f-106">Метод Ивмдрмевентженератор:: Канцеласинкоператион</span><span class="sxs-lookup"><span data-stu-id="a8a9f-106">IWMDRMEventGenerator::CancelAsyncOperation method</span></span>

<span data-ttu-id="a8a9f-107">Метод **канцеласинкоператион** отменяет асинхронную операцию.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-107">The **CancelAsyncOperation** method cancels an asynchronous operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8a9f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a8a9f-108">Syntax</span></span>


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="a8a9f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a8a9f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8a9f-110">*пункканцелатионкукие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a8a9f-110">*punkCancelationCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8a9f-111">Указатель на файл cookie отмены, определяющий асинхронную операцию, которая должна быть отменена.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-111">Pointer to the cancellation cookie that identifies the asynchronous operation to be canceled.</span></span> <span data-ttu-id="a8a9f-112">Этот файл cookie предоставляется методом, используемым для запуска операции.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-112">This cookie is provided by the method used to start the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8a9f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a8a9f-113">Return value</span></span>

<span data-ttu-id="a8a9f-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a8a9f-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a8a9f-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a8a9f-116">Return code</span></span>                                                                          | <span data-ttu-id="a8a9f-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a8a9f-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a8a9f-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a8a9f-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a8a9f-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-119">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a8a9f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a8a9f-120">Remarks</span></span>

<span data-ttu-id="a8a9f-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="a8a9f-121">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8a9f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a8a9f-122">Requirements</span></span>



| <span data-ttu-id="a8a9f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a8a9f-123">Requirement</span></span> | <span data-ttu-id="a8a9f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a8a9f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8a9f-125">Header</span><span class="sxs-lookup"><span data-stu-id="a8a9f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a8a9f-126"><dt>Вмдрмсдк. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8a9f-126"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8a9f-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a8a9f-127">Library</span></span><br/> | <dl> <span data-ttu-id="a8a9f-128"><dt>Вмдрмсдк. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8a9f-128"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8a9f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8a9f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8a9f-130">**Интерфейс Ивмдрмевентженератор**</span><span class="sxs-lookup"><span data-stu-id="a8a9f-130">**IWMDRMEventGenerator Interface**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





