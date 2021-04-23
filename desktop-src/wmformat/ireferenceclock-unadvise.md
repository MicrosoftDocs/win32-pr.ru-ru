---
title: Иреференцеклокк метод unadvise
description: Метод unadvise отменяет запрос уведомления.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Метод Unadvise для Windows Media Format
- Метод Unadvise для Windows Media Format, интерфейс Иреференцеклокк
- Иреференцеклокк интерфейса Windows Media Format, метод unadvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104133239"
---
# <a name="ireferenceclockunadvise-method"></a><span data-ttu-id="2ff28-106">Метод Иреференцеклокк:: unadvise</span><span class="sxs-lookup"><span data-stu-id="2ff28-106">IReferenceClock::Unadvise method</span></span>

<span data-ttu-id="2ff28-107">Метод **unadvise** отменяет запрос уведомления.</span><span class="sxs-lookup"><span data-stu-id="2ff28-107">The **Unadvise** method cancels a notification request.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff28-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ff28-108">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="2ff28-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ff28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff28-110">*двадвисекукие*</span><span class="sxs-lookup"><span data-stu-id="2ff28-110">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="2ff28-111">Идентификатор удаляемого запроса.</span><span class="sxs-lookup"><span data-stu-id="2ff28-111">Identifier of the request to remove.</span></span> <span data-ttu-id="2ff28-112">Используйте значение, возвращаемое функцией Адвисетиме, в параметре Пдвадвисекукие.</span><span class="sxs-lookup"><span data-stu-id="2ff28-112">Use the value returned by AdviseTime in the pdwAdviseCookie parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff28-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ff28-113">Return value</span></span>

<span data-ttu-id="2ff28-114">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2ff28-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2ff28-115">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="2ff28-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2ff28-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2ff28-116">Return code</span></span>                                                                             | <span data-ttu-id="2ff28-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2ff28-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="2ff28-118"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2ff28-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2ff28-119">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="2ff28-119">The method succeeded.</span></span><br/>                    |
| <dl> <span data-ttu-id="2ff28-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2ff28-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2ff28-121">Переданный идентификатор не существует.</span><span class="sxs-lookup"><span data-stu-id="2ff28-121">The identifier passed in does not exist.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="2ff28-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ff28-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff28-123">**Интерфейс Иреференцеклокк**</span><span class="sxs-lookup"><span data-stu-id="2ff28-123">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





