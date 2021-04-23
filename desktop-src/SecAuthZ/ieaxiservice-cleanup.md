---
description: Освобождает ресурсы, используемые интерфейсом Иеаксисервице.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'Метод Иеаксисервице:: Cleanup'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265643"
---
# <a name="ieaxiservicecleanup-method"></a><span data-ttu-id="0b6e7-103">Метод Иеаксисервице:: Cleanup</span><span class="sxs-lookup"><span data-stu-id="0b6e7-103">IeAxiService::Cleanup method</span></span>

<span data-ttu-id="0b6e7-104">Метод **Cleanup** освобождает ресурсы, используемые интерфейсом [**иеаксисервице**](ieaxiservice.md) .</span><span class="sxs-lookup"><span data-stu-id="0b6e7-104">The **Cleanup** method frees resources used by the [**IeAxiService**](ieaxiservice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b6e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b6e7-105">Syntax</span></span>


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a><span data-ttu-id="0b6e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b6e7-106">Parameters</span></span>

<span data-ttu-id="0b6e7-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0b6e7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0b6e7-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0b6e7-108">Return value</span></span>

<span data-ttu-id="0b6e7-109">Если метод завершается успешно, метод возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0b6e7-109">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="0b6e7-110">Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="0b6e7-110">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="0b6e7-111">Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).</span><span class="sxs-lookup"><span data-stu-id="0b6e7-111">For a list of common error codes, see [Common HRESULT Values](/windows/desktop/SecCrypto/common-hresult-values).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b6e7-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0b6e7-112">Requirements</span></span>



| <span data-ttu-id="0b6e7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0b6e7-113">Requirement</span></span> | <span data-ttu-id="0b6e7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0b6e7-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b6e7-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0b6e7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0b6e7-116">Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="0b6e7-116">Windows Vista Business, Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0b6e7-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0b6e7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0b6e7-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0b6e7-118">None supported</span></span><br/>                                                                                 |
| <span data-ttu-id="0b6e7-119">IID</span><span class="sxs-lookup"><span data-stu-id="0b6e7-119">IID</span></span><br/>                      | <span data-ttu-id="0b6e7-120">IID \_ иеаксисервице определен как E9E92380-9ECD-4982-A0EB-6815A56CCF27</span><span class="sxs-lookup"><span data-stu-id="0b6e7-120">IID\_IeAxiService is defined as E9E92380-9ECD-4982-A0EB-6815A56CCF27</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="0b6e7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b6e7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b6e7-122">**иеаксисервице**</span><span class="sxs-lookup"><span data-stu-id="0b6e7-122">**IeAxiService**</span></span>](ieaxiservice.md)
</dt> </dl>

 

