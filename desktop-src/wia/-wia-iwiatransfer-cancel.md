---
description: Отменяет текущую операцию перемещения.
ms.assetid: 42c6b2c3-7b6a-45d2-a7ce-844e95fe277b
title: 'Метод Ивиатрансфер:: Cancel (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.Cancel
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 4764e922498a3c33278555cae37d09c1822959dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541970"
---
# <a name="iwiatransfercancel-method"></a><span data-ttu-id="663bb-103">Метод Ивиатрансфер:: Cancel</span><span class="sxs-lookup"><span data-stu-id="663bb-103">IWiaTransfer::Cancel method</span></span>

<span data-ttu-id="663bb-104">Отменяет текущую операцию перемещения.</span><span class="sxs-lookup"><span data-stu-id="663bb-104">Cancels the current transfer operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="663bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="663bb-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="663bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="663bb-106">Parameters</span></span>

<span data-ttu-id="663bb-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="663bb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="663bb-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="663bb-108">Return value</span></span>

<span data-ttu-id="663bb-109">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="663bb-109">Type: **HRESULT**</span></span>

<span data-ttu-id="663bb-110">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="663bb-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="663bb-111">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="663bb-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="663bb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="663bb-112">Requirements</span></span>



| <span data-ttu-id="663bb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="663bb-113">Requirement</span></span> | <span data-ttu-id="663bb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="663bb-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="663bb-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="663bb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="663bb-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="663bb-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="663bb-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="663bb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="663bb-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="663bb-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="663bb-119">Header</span><span class="sxs-lookup"><span data-stu-id="663bb-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="663bb-120"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="663bb-120"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="663bb-121">IDL</span><span class="sxs-lookup"><span data-stu-id="663bb-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="663bb-122"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="663bb-122"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="663bb-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="663bb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="663bb-124"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="663bb-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




