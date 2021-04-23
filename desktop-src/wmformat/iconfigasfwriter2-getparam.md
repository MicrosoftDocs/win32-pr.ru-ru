---
title: IConfigAsfWriter2, метод
description: Метод param извлекает текущее значение указанного параметра конфигурации фильтра.
ms.assetid: 81d915a1-6190-46e3-a5cb-7f5fc242b8dd
keywords:
- Метод param Windows Media Format
- Метод param, формат Windows Media Format, интерфейс IConfigAsfWriter2
- Интерфейс IConfigAsfWriter2 интерфейса Windows Media Format, метод param
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.GetParam
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d72b8011072424679729686dd5a14c92bae90f66
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105691618"
---
# <a name="iconfigasfwriter2getparam-method"></a><span data-ttu-id="d191e-106">Метод IConfigAsfWriter2:: param</span><span class="sxs-lookup"><span data-stu-id="d191e-106">IConfigAsfWriter2::GetParam method</span></span>

<span data-ttu-id="d191e-107">Метод **param** извлекает текущее значение указанного параметра конфигурации фильтра.</span><span class="sxs-lookup"><span data-stu-id="d191e-107">The **GetParam** method retrieves the current value of the specified filter configuration parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d191e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d191e-108">Syntax</span></span>


```C++
HRESULT GetParam(
  [in]  DWORD dwParam,
  [out] DWORD *pdwParam1,
  [out] DWORD *pdwParam2
);
```



## <a name="parameters"></a><span data-ttu-id="d191e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d191e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d191e-110">*двпарам* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d191e-110">*dwParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d191e-111">Указывает параметр для извлечения.</span><span class="sxs-lookup"><span data-stu-id="d191e-111">Specifies the parameter to retrieve.</span></span> <span data-ttu-id="d191e-112">Оно должно быть значением, определенным в перечислении [ \_ \_ \_ param асфвритерконфиг](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d191e-112">It must be a value defined in the [\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85)) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="d191e-113">*pdwParam1* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d191e-113">*pdwParam1* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d191e-114">Указатель на переменную, которая получает значение параметра, указанного в *двпарам*.</span><span class="sxs-lookup"><span data-stu-id="d191e-114">Pointer to a variable that retrieves the value of the parameter specified in *dwParam*.</span></span>

</dd> <dt>

<span data-ttu-id="d191e-115">*pdwParam2* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d191e-115">*pdwParam2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d191e-116">Не используется, должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d191e-116">Not used, must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d191e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d191e-117">Return value</span></span>

<span data-ttu-id="d191e-118">Если метод завершается успешно, возвращается значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d191e-118">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="d191e-119">В случае сбоя возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d191e-119">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="d191e-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d191e-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="d191e-121">[**Интерфейс IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d191e-121">[**IConfigAsfWriter2 Interface**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d191e-122">**IConfigAsfWriter2:: Сетпарам**</span><span class="sxs-lookup"><span data-stu-id="d191e-122">**IConfigAsfWriter2::SetParam**</span></span>](iconfigasfwriter2-setparam.md)
</dt> </dl>

 

 