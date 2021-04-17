---
title: Ивмдрмдевице Клеандатасторе, метод
description: Метод Клеандатасторе запускает процесс очистки хранилища данных DRM на устройстве.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Метод Клеандатасторе Windows Media диспетчер устройств
- Метод Клеандатасторе Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Клеандатасторе
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5aed9608a7428245edd84602ea5e7252861d938
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694423"
---
# <a name="iwmdrmdevicecleandatastore-method"></a><span data-ttu-id="a6fb1-106">Метод Ивмдрмдевице:: Клеандатасторе</span><span class="sxs-lookup"><span data-stu-id="a6fb1-106">IWMDRMDevice::CleanDataStore method</span></span>

<span data-ttu-id="a6fb1-107">Метод **клеандатасторе** запускает процесс очистки хранилища данных DRM на устройстве.</span><span class="sxs-lookup"><span data-stu-id="a6fb1-107">The **CleanDataStore** method starts the process of cleaning the DRM data store on the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6fb1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6fb1-108">Syntax</span></span>


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a6fb1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6fb1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6fb1-110">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6fb1-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6fb1-111">Флаги для критериев очистки хранилища.</span><span class="sxs-lookup"><span data-stu-id="a6fb1-111">Flags for store cleaning criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6fb1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6fb1-112">Return value</span></span>

<span data-ttu-id="a6fb1-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a6fb1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a6fb1-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a6fb1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a6fb1-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="a6fb1-115">Return code</span></span>                                                                          | <span data-ttu-id="a6fb1-116">Описание</span><span class="sxs-lookup"><span data-stu-id="a6fb1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a6fb1-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="a6fb1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a6fb1-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="a6fb1-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a6fb1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a6fb1-119">Requirements</span></span>



| <span data-ttu-id="a6fb1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a6fb1-120">Requirement</span></span> | <span data-ttu-id="a6fb1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a6fb1-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a6fb1-122">Header</span><span class="sxs-lookup"><span data-stu-id="a6fb1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a6fb1-123"><dt>ВМДДРМСП. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6fb1-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="a6fb1-124">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a6fb1-124">Library</span></span><br/> | <dl> <span data-ttu-id="a6fb1-125"><dt>Мссачлп. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a6fb1-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6fb1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6fb1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6fb1-127">**Интерфейс Ивмдрмдевице**</span><span class="sxs-lookup"><span data-stu-id="a6fb1-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





