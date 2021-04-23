---
title: IConfigAsfWriter2 Ресетмултипассстате, метод
description: Метод Ресетмултипассстате сбрасывает фильтр, когда этап кодирования предварительной обработки отменяется до его завершения.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Формат Windows Media, Ресетмултипассстате метод
- Ресетмултипассстате метод Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 Windows Media Format, метод Ресетмултипассстате
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413450"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a><span data-ttu-id="f11c4-106">Метод IConfigAsfWriter2:: Ресетмултипассстате</span><span class="sxs-lookup"><span data-stu-id="f11c4-106">IConfigAsfWriter2::ResetMultiPassState method</span></span>

<span data-ttu-id="f11c4-107">Метод **ресетмултипассстате** сбрасывает фильтр, когда этап кодирования предварительной обработки отменяется до его завершения.</span><span class="sxs-lookup"><span data-stu-id="f11c4-107">The **ResetMultiPassState** method resets the filter when a preprocessing encoding pass is canceled before it is completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11c4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f11c4-108">Syntax</span></span>


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a><span data-ttu-id="f11c4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f11c4-109">Parameters</span></span>

<span data-ttu-id="f11c4-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="f11c4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f11c4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f11c4-111">Return value</span></span>

<span data-ttu-id="f11c4-112">Метод возвращает **значение HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f11c4-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f11c4-113">Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f11c4-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f11c4-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f11c4-114">Return code</span></span>                                                                                         | <span data-ttu-id="f11c4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f11c4-115">Description</span></span>                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="f11c4-116"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f11c4-116"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="f11c4-117">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="f11c4-117">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="f11c4-118"><dt>**VFW \_ E \_ не \_ остановлен**</dt></span><span class="sxs-lookup"><span data-stu-id="f11c4-118"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="f11c4-119">Фильтр не находится в остановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="f11c4-119">The filter was not in a stopped state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f11c4-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f11c4-120">Remarks</span></span>

<span data-ttu-id="f11c4-121">Этот метод должен вызываться для сброса внутреннего состояния фильтра при отмене этапа кодирования предварительной обработки до того, как фильтр получил событие **\_ \_ завершения предварительной обработки** .</span><span class="sxs-lookup"><span data-stu-id="f11c4-121">This method must be called to reset the internal state of the filter whenever a preprocessing encoding pass is canceled before the filter has received an **EC\_PREPROCESS\_COMPLETE** event.</span></span> <span data-ttu-id="f11c4-122">Нет необходимости вызывать этот метод, если процесс кодирования предварительной обработки завершается без ошибок.</span><span class="sxs-lookup"><span data-stu-id="f11c4-122">It is not necessary to call this method if the preprocessing encoding pass completes without errors.</span></span>

## <a name="see-also"></a><span data-ttu-id="f11c4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f11c4-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="f11c4-124">[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f11c4-124">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> </dl>

 

