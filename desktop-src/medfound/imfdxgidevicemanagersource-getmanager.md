---
description: Возвращает Имфдксгидевицеманажер из приемника отрисовки Microsoft Media Foundation видео.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'Метод Имфдксгидевицеманажерсаурце:: Manage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692931"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a><span data-ttu-id="791d0-103">Метод Имфдксгидевицеманажерсаурце:: Manage</span><span class="sxs-lookup"><span data-stu-id="791d0-103">IMFDXGIDeviceManagerSource::GetManager method</span></span>

<span data-ttu-id="791d0-104">Возвращает [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) из приемника отрисовки Microsoft Media Foundation видео.</span><span class="sxs-lookup"><span data-stu-id="791d0-104">Gets the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) from the Microsoft Media Foundation video rendering sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="791d0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="791d0-105">Syntax</span></span>


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="791d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="791d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="791d0-107">*ппманажер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="791d0-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="791d0-108">Объект [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="791d0-108">The [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="791d0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="791d0-109">Return value</span></span>

<span data-ttu-id="791d0-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="791d0-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="791d0-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="791d0-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="791d0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="791d0-112">Requirements</span></span>



| <span data-ttu-id="791d0-113">Требование</span><span class="sxs-lookup"><span data-stu-id="791d0-113">Requirement</span></span> | <span data-ttu-id="791d0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="791d0-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="791d0-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="791d0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="791d0-116">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="791d0-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="791d0-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="791d0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="791d0-118">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="791d0-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="791d0-119">IDL</span><span class="sxs-lookup"><span data-stu-id="791d0-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="791d0-120"><dt>Мфидл. idl</dt></span><span class="sxs-lookup"><span data-stu-id="791d0-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="791d0-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="791d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="791d0-122">**имфдксгидевицеманажерсаурце**</span><span class="sxs-lookup"><span data-stu-id="791d0-122">**IMFDXGIDeviceManagerSource**</span></span>](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




