---
title: Ивмдрмлиценсе Жетаутпутпротектионлевелс, метод
description: Метод Жетаутпутпротектионлевелс извлекает сведения обо всех уровнях защиты выходных данных (Оплс), назначенных лицензии.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Формат Windows Media, Жетаутпутпротектионлевелс метод
- Жетаутпутпротектионлевелс метод Windows Media Format, интерфейс Ивмдрмлиценсе
- Интерфейс Ивмдрмлиценсе Windows Media Format, метод Жетаутпутпротектионлевелс
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "105700737"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a><span data-ttu-id="7f9da-106">Метод Ивмдрмлиценсе:: Жетаутпутпротектионлевелс</span><span class="sxs-lookup"><span data-stu-id="7f9da-106">IWMDRMLicense::GetOutputProtectionLevels method</span></span>

<span data-ttu-id="7f9da-107">Метод **жетаутпутпротектионлевелс** извлекает сведения обо всех уровнях защиты выходных данных (оплс), назначенных лицензии.</span><span class="sxs-lookup"><span data-stu-id="7f9da-107">The **GetOutputProtectionLevels** method retrieves information about all output protection levels (OPLs) assigned to the license.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f9da-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f9da-108">Syntax</span></span>


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a><span data-ttu-id="7f9da-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f9da-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f9da-110">*поплс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7f9da-110">*pOPLs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f9da-111">Указатель на структуру [**\_ \_ \_ уровней защиты данных WMDRM**](wmdrm-output-protection-levels.md) , которая получает сведения о ОПЛ.</span><span class="sxs-lookup"><span data-stu-id="7f9da-111">Pointer to a [**WMDRM\_OUTPUT\_PROTECTION\_LEVELS**](wmdrm-output-protection-levels.md) structure that receives the OPL information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f9da-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f9da-112">Return value</span></span>

<span data-ttu-id="7f9da-113">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7f9da-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7f9da-114">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7f9da-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7f9da-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7f9da-115">Return code</span></span>                                                                          | <span data-ttu-id="7f9da-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7f9da-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="7f9da-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7f9da-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7f9da-118">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="7f9da-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f9da-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f9da-119">Remarks</span></span>

<span data-ttu-id="7f9da-120">Нет.</span><span class="sxs-lookup"><span data-stu-id="7f9da-120">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f9da-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f9da-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f9da-122">**Интерфейс Ивмдрмлиценсе**</span><span class="sxs-lookup"><span data-stu-id="7f9da-122">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





