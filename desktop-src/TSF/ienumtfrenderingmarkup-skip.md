---
title: Метод Skip Иенумтфрендерингмаркуп
description: Метод Skip Иенумтфрендерингмаркуп получает от текущей позицией указанное число элементов в последовательности перечисления.
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Метод Skip Text Services Framework
- Метод Skip Text Services Framework, интерфейс Иенумтфрендерингмаркуп
- Платформа текстовых служб с интерфейсом Иенумтфрендерингмаркуп, метод Skip
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783708"
---
# <a name="ienumtfrenderingmarkupskip-method"></a><span data-ttu-id="5864f-106">Метод Иенумтфрендерингмаркуп:: Skip</span><span class="sxs-lookup"><span data-stu-id="5864f-106">IEnumTfRenderingMarkup::Skip method</span></span>

<span data-ttu-id="5864f-107">Метод **иенумтфрендерингмаркуп:: Skip** получает от текущей позицией указанное число элементов в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="5864f-107">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="5864f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5864f-108">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a><span data-ttu-id="5864f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5864f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5864f-110">*улкаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5864f-110">*ulCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5864f-111">\[в параметре \] указывает количество элементов для пропуска.</span><span class="sxs-lookup"><span data-stu-id="5864f-111">\[in\] Specifies the number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5864f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5864f-112">Return value</span></span>

<span data-ttu-id="5864f-113">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="5864f-113">This method can return one of these values.</span></span>



| <span data-ttu-id="5864f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="5864f-114">Value</span></span>                                                                                   | <span data-ttu-id="5864f-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5864f-115">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5864f-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5864f-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5864f-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="5864f-117">The method was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="5864f-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="5864f-118"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5864f-119">Метод достиг конца перечисления, прежде чем заданное число элементов может быть пропущено.</span><span class="sxs-lookup"><span data-stu-id="5864f-119">The method reached the end of the enumeration before the specified number of elements could be skipped.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5864f-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5864f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5864f-121">Этот метод в настоящее время не находится в файлах общедоступного заголовка.</span><span class="sxs-lookup"><span data-stu-id="5864f-121">This method is not currently in the public header files.</span></span> <span data-ttu-id="5864f-122">Чтобы использовать этот API, необходимо скомпилировать [прототип](prototypes.md)с помощью MIDL.</span><span class="sxs-lookup"><span data-stu-id="5864f-122">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 





