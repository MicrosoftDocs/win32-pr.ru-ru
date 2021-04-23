---
title: Ибасикдевице Ремотестреамингурлс, метод
description: Возвращает вектор URL-адресов удаленной потоковой передачи.
ms.assetid: 19B4475F-A7E4-4DC4-9C88-68D91D023AF4
keywords:
- API потоковой передачи мультимедиа метода Ремотестреамингурлс
- API потоковой передачи мультимедиа метода Ремотестреамингурлс, интерфейс Ибасикдевице
- API потоковой передачи мультимедиа интерфейса Ибасикдевице, метод Ремотестреамингурлс
topic_type:
- apiref
api_name:
- IBasicDevice.RemoteStreamingUrls
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdc4bd363096e7b808a51cfbddb764daabe03a55
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411761"
---
# <a name="ibasicdeviceremotestreamingurls-method"></a><span data-ttu-id="4dd41-106">Метод Ибасикдевице:: Ремотестреамингурлс</span><span class="sxs-lookup"><span data-stu-id="4dd41-106">IBasicDevice::RemoteStreamingUrls method</span></span>

<span data-ttu-id="4dd41-107">Возвращает вектор URL-адресов удаленной потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="4dd41-107">Returns a vector of remote streaming URLs.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd41-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dd41-108">Syntax</span></span>


```C++
HRESULT RemoteStreamingUrls(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="4dd41-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dd41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dd41-110">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4dd41-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4dd41-111">Получает перечисляемую коллекцию указателей на URL-адреса удаленной потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="4dd41-111">Receives an enumerable collection of pointers to remote streaming URLs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dd41-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dd41-112">Return value</span></span>

<span data-ttu-id="4dd41-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4dd41-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4dd41-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4dd41-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4dd41-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4dd41-115">Return code</span></span>                                                                          | <span data-ttu-id="4dd41-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4dd41-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4dd41-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4dd41-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4dd41-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4dd41-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4dd41-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4dd41-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dd41-120">**ибасикдевице**</span><span class="sxs-lookup"><span data-stu-id="4dd41-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





