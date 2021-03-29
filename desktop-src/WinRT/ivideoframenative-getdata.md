---
description: Этот метод возвращает интерфейс, предоставляющий доступ к данным видео.
ms.assetid: 084F020F-A6F5-4982-BA4B-A8F8D6182868
title: 'Метод Ивидеофраменативе:: GetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVideoFrameNative.GetData
api_type:
- COM
api_location:
- windows.media.core.interop.h
ms.openlocfilehash: c612d2d34e23b393921f83f7dbe9e189aa366b30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991120"
---
# <a name="ivideoframenativegetdata-method"></a><span data-ttu-id="50299-103">Метод Ивидеофраменативе:: GetData</span><span class="sxs-lookup"><span data-stu-id="50299-103">IVideoFrameNative::GetData method</span></span>

<span data-ttu-id="50299-104">Этот метод возвращает интерфейс, предоставляющий доступ к данным видео.</span><span class="sxs-lookup"><span data-stu-id="50299-104">This method returns an interface that provides access to the video data.</span></span>

## <a name="syntax"></a><span data-ttu-id="50299-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50299-105">Syntax</span></span>


```C++
HRESULT GetData(
  [in]  REFIID riid,
  [out] LPVOID *ppv
);
```



## <a name="parameters"></a><span data-ttu-id="50299-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="50299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50299-107">*riid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50299-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50299-108">IID получаемого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="50299-108">The IID of the interface to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="50299-109">*ППВ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="50299-109">*ppv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50299-110">При успешном возврате этого метода содержит указатель интерфейса, запрошенный в параметре *riid* .</span><span class="sxs-lookup"><span data-stu-id="50299-110">When this method returns successfully, contains the interface pointer requested in *riid* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50299-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50299-111">Return value</span></span>

<span data-ttu-id="50299-112">Возвращает \_ ОК при успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="50299-112">Returns S\_OK on successful completion.</span></span> <span data-ttu-id="50299-113">Возвращает E \_ Interface, если не удается найти запрошенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="50299-113">Returns E\_NOINTERFACE if the requested interface can't be found.</span></span>

## <a name="see-also"></a><span data-ttu-id="50299-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50299-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50299-115">**ивидеофраменативе**</span><span class="sxs-lookup"><span data-stu-id="50299-115">**IVideoFrameNative**</span></span>](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative)
</dt> </dl>

 

 



