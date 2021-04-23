---
description: Возвращает Имеморибуффер в виде массива байтов.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Метод Имеморибуффербитеакцесс:: with buffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711059"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a><span data-ttu-id="7d713-103">Метод Имеморибуффербитеакцесс:: with buffer</span><span class="sxs-lookup"><span data-stu-id="7d713-103">IMemoryBufferByteAccess::GetBuffer method</span></span>

<span data-ttu-id="7d713-104">Возвращает [**имеморибуффер**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) в виде массива байтов.</span><span class="sxs-lookup"><span data-stu-id="7d713-104">Gets an [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) as an array of bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d713-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d713-105">Syntax</span></span>


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a><span data-ttu-id="7d713-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d713-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d713-107">*значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7d713-107">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d713-108">Указатель на массив байтов, содержащий данные буфера.</span><span class="sxs-lookup"><span data-stu-id="7d713-108">A pointer to a byte array containing the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="7d713-109">*емкость* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7d713-109">*capacity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d713-110">Число байтов в возвращаемом массиве</span><span class="sxs-lookup"><span data-stu-id="7d713-110">The number of bytes in the returned array</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d713-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d713-111">Return value</span></span>

<span data-ttu-id="7d713-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7d713-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d713-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d713-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d713-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d713-114">Remarks</span></span>

<span data-ttu-id="7d713-115">При вызове [**параметр memorybuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) код, использующий этот буфер, должен установить указатель на *значение* null.</span><span class="sxs-lookup"><span data-stu-id="7d713-115">When [**MemoryBuffer::Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) is called, the code using this buffer should set the *value* pointer to null.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d713-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d713-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d713-117">[**имеморибуффербитеакцесс**](/previous-versions//mt297505(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d713-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span></span>
</dt> </dl>

 

 
