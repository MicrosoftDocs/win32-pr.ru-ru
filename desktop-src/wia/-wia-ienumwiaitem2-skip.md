---
description: Пропускает указанное число элементов во время перечисления доступных объектов IWiaItem2.
ms.assetid: 7a5e9e1c-1e6e-4de0-9499-bf89e35c19aa
title: 'Метод IEnumWiaItem2:: Skip (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Skip
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7618aad923136a9a32d8b7fb935050fefe07bff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991279"
---
# <a name="ienumwiaitem2skip-method"></a><span data-ttu-id="755d8-103">Метод IEnumWiaItem2:: Skip</span><span class="sxs-lookup"><span data-stu-id="755d8-103">IEnumWiaItem2::Skip method</span></span>

<span data-ttu-id="755d8-104">Пропускает указанное число элементов во время перечисления доступных объектов [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="755d8-104">Skips the specified number of items during an enumeration of available [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="755d8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="755d8-105">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG cElt
);
```



## <a name="parameters"></a><span data-ttu-id="755d8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="755d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="755d8-107">*cElt* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="755d8-107">*cElt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="755d8-108">Тип: **ulong**</span><span class="sxs-lookup"><span data-stu-id="755d8-108">Type: **ULONG**</span></span>

<span data-ttu-id="755d8-109">Указывает число пропускаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="755d8-109">Specifies the number of items to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="755d8-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="755d8-110">Return value</span></span>

<span data-ttu-id="755d8-111">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="755d8-111">Type: **HRESULT**</span></span>

<span data-ttu-id="755d8-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="755d8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="755d8-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="755d8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="755d8-114">Требования</span><span class="sxs-lookup"><span data-stu-id="755d8-114">Requirements</span></span>



| <span data-ttu-id="755d8-115">Требование</span><span class="sxs-lookup"><span data-stu-id="755d8-115">Requirement</span></span> | <span data-ttu-id="755d8-116">Значение</span><span class="sxs-lookup"><span data-stu-id="755d8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="755d8-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="755d8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="755d8-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="755d8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="755d8-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="755d8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="755d8-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="755d8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="755d8-121">Header</span><span class="sxs-lookup"><span data-stu-id="755d8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="755d8-122"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="755d8-122"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="755d8-123">IDL</span><span class="sxs-lookup"><span data-stu-id="755d8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="755d8-124"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="755d8-124"><dt>Wia.idl</dt></span></span> </dl> |



 

 




