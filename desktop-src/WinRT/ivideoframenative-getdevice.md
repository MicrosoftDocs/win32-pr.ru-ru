---
description: Этот метод возвращает устройство, связанное с данными видео.
ms.assetid: 9A61159B-C383-4770-AD8F-9F69F720E3E2
title: 'Метод Ивидеофраменативе:: of Device'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetDevice
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: d012ae79b1cb2c83e916dc74113cc3d0560da4c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423785"
---
# <a name="ivideoframenativegetdevice-method"></a><span data-ttu-id="a82ff-103">Метод Ивидеофраменативе:: of Device</span><span class="sxs-lookup"><span data-stu-id="a82ff-103">IVideoFrameNative::GetDevice method</span></span>

<span data-ttu-id="a82ff-104">Этот метод возвращает устройство, связанное с данными видео.</span><span class="sxs-lookup"><span data-stu-id="a82ff-104">This method returns a device associated with the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a82ff-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="a82ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a82ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a82ff-107">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a82ff-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82ff-108">Идентификатор IID извлекаемого устройства.</span><span class="sxs-lookup"><span data-stu-id="a82ff-108">The IID of the device to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a82ff-109">*ППВ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a82ff-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a82ff-110">При успешном возврате этого метода содержит указатель устройства, запрошенный в параметре *riid* .</span><span class="sxs-lookup"><span data-stu-id="a82ff-110">When this method returns successfully, contains the device pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a82ff-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a82ff-111">Return value</span></span>

<span data-ttu-id="a82ff-112">Возвращает \_ ОК при успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="a82ff-112">Returns S\_OK on successful completion.</span></span>

## <a name="see-also"></a><span data-ttu-id="a82ff-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a82ff-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82ff-114">**ивидеофраменативе**</span><span class="sxs-lookup"><span data-stu-id="a82ff-114">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



