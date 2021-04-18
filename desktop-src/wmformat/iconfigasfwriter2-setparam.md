---
title: IConfigAsfWriter2 Сетпарам, метод
description: Метод Сетпарам задает значение указанного параметра конфигурации фильтра.
ms.assetid: b8067fb2-c379-4b26-b4f7-c790604e3edc
keywords:
- Формат Windows Media, Сетпарам метод
- Сетпарам метод Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 Windows Media Format, метод Сетпарам
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.SetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f123bf11c8297f3a7ce0d4b0047874d8d7b31b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691598"
---
# <a name="iconfigasfwriter2setparam-method"></a><span data-ttu-id="59243-106">Метод IConfigAsfWriter2:: Сетпарам</span><span class="sxs-lookup"><span data-stu-id="59243-106">IConfigAsfWriter2::SetParam method</span></span>

<span data-ttu-id="59243-107">Метод **сетпарам** задает значение указанного параметра конфигурации фильтра.</span><span class="sxs-lookup"><span data-stu-id="59243-107">The **SetParam** method sets the value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="59243-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59243-108">Syntax</span></span>


```C++
HRESULT SetParam(
  [in] DWORD dwParam,
  [in] DWORD dwParam1,
  [in] DWORD dwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="59243-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59243-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59243-110">*двпарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59243-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59243-111">Задает заданный параметр.</span><span class="sxs-lookup"><span data-stu-id="59243-111">Specifies the parameter to set.</span></span> <span data-ttu-id="59243-112">Оно должно быть значением, определенным в перечислении [ \_ \_ \_ param асфвритерконфиг](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="59243-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="59243-113">*dwParam1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59243-113">*dwParam1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59243-114">Указывает значение, присваиваемое параметру *двпарам* .</span><span class="sxs-lookup"><span data-stu-id="59243-114">Specifies the value to assign to the *dwParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="59243-115">*dwParam2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59243-115">*dwParam2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59243-116">Не используется; значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="59243-116">Not used; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59243-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59243-117">Return value</span></span>

<span data-ttu-id="59243-118">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="59243-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="59243-119">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="59243-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="59243-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59243-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="59243-121">[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59243-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="59243-122">**IConfigAsfWriter2:: param**</span><span class="sxs-lookup"><span data-stu-id="59243-122">**IConfigAsfWriter2::GetParam**</span></span>](iconfigasfwriter2-getparam.md)
</dt> </dl>

 

 