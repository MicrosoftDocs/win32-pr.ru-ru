---
description: Сбрасывает ссылку перечисления на первый объект IWiaItem2.
ms.assetid: 392e3471-f7fc-456f-a1cc-ab4eb6d3fe18
title: 'Метод IEnumWiaItem2:: Reset (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Reset
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: ab4d5a9effbcb003265da53ddc753f63630df51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263313"
---
# <a name="ienumwiaitem2reset-method"></a><span data-ttu-id="a704f-103">Метод IEnumWiaItem2:: Reset</span><span class="sxs-lookup"><span data-stu-id="a704f-103">IEnumWiaItem2::Reset method</span></span>

<span data-ttu-id="a704f-104">Сбрасывает ссылку перечисления на первый объект [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="a704f-104">Resets the enumeration reference to the first [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a704f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a704f-105">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="a704f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a704f-106">Parameters</span></span>

<span data-ttu-id="a704f-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a704f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a704f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a704f-108">Return value</span></span>

<span data-ttu-id="a704f-109">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a704f-109">Type: **HRESULT**</span></span>

<span data-ttu-id="a704f-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="a704f-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a704f-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a704f-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a704f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a704f-112">Requirements</span></span>



| <span data-ttu-id="a704f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="a704f-113">Requirement</span></span> | <span data-ttu-id="a704f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a704f-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a704f-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a704f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a704f-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a704f-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a704f-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a704f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a704f-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a704f-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a704f-119">Header</span><span class="sxs-lookup"><span data-stu-id="a704f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a704f-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="a704f-120"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="a704f-121">IDL</span><span class="sxs-lookup"><span data-stu-id="a704f-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a704f-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a704f-122"><dt>Wia.idl</dt></span></span> </dl> |



 

 




