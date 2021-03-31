---
title: Медиарендерер. Стопасинк, метод
description: Указывает ДМР асинхронно закончить воспроизведение текущего содержимого. | Медиарендерер. Стопасинк, метод
ms.assetid: 04cf6d5a-8aa5-4821-8117-f250bfaf7ebd
keywords:
- API потоковой передачи мультимедиа метода Стопасинк
- API потоковой передачи мультимедиа метода Стопасинк, интерфейс Медиарендерер
- API потоковой передачи мультимедиа интерфейса Медиарендерер, метод Стопасинк
topic_type:
- apiref
api_name:
- MediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 205c69a83572539974c1b8ad2cf45159c45335cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104157107"
---
# <a name="mediarendererstopasync-method"></a><span data-ttu-id="b2c64-107">Медиарендерер. Стопасинк, метод</span><span class="sxs-lookup"><span data-stu-id="b2c64-107">MediaRenderer.StopAsync method</span></span>

<span data-ttu-id="b2c64-108">Указывает ДМР асинхронно закончить воспроизведение текущего содержимого.</span><span class="sxs-lookup"><span data-stu-id="b2c64-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2c64-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2c64-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="b2c64-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2c64-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2c64-111">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b2c64-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2c64-112">Получает ссылку на объект [**плайбаккоператион**](playbackoperation.md) , используемый для получения результатов асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="b2c64-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2c64-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b2c64-113">Return value</span></span>

<span data-ttu-id="b2c64-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b2c64-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b2c64-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b2c64-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b2c64-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b2c64-116">Return code</span></span>                                                                          | <span data-ttu-id="b2c64-117">Описание</span><span class="sxs-lookup"><span data-stu-id="b2c64-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b2c64-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b2c64-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b2c64-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="b2c64-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="b2c64-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2c64-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c64-121">**медиарендерер**</span><span class="sxs-lookup"><span data-stu-id="b2c64-121">**MediaRenderer**</span></span>](mediarenderer.md)
</dt> </dl>

 

 





