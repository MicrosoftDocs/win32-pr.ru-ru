---
description: Метод PROPS извлекает свойства, заданные для этого объекта, с соответствующими значениями.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: Метод Ипропертисеттер::-PROPS (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685217"
---
# <a name="ipropertysettergetprops-method"></a><span data-ttu-id="1ec6c-103">Метод Ипропертисеттер:: Props</span><span class="sxs-lookup"><span data-stu-id="1ec6c-103">IPropertySetter::GetProps method</span></span>

> [!Note]  
> <span data-ttu-id="1ec6c-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-104">\[Deprecated.</span></span> <span data-ttu-id="1ec6c-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1ec6c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="1ec6c-106">`GetProps`Метод получает свойства, заданные для этого объекта, с соответствующими значениями.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-106">The `GetProps` method retrieves the properties set on this object, with their corresponding values.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec6c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1ec6c-107">Syntax</span></span>


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a><span data-ttu-id="1ec6c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ec6c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec6c-109">*пкпарамс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1ec6c-109">*pcParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec6c-110">Получает количество структур, возвращенных в *папарам*.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-110">Receives the number of structures returned in *paParam*.</span></span>

</dd> <dt>

<span data-ttu-id="1ec6c-111">*папарам* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1ec6c-111">*paParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec6c-112">Адрес указателя на массив структур [**\_ param Декстер**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec6c-112">Address of a pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="1ec6c-113">*павалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1ec6c-113">*paValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec6c-114">Адрес указателя на массив структур [**\_ значений Декстер**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec6c-114">Address of a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec6c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1ec6c-115">Return value</span></span>

<span data-ttu-id="1ec6c-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1ec6c-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1ec6c-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec6c-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ec6c-118">Remarks</span></span>

<span data-ttu-id="1ec6c-119">Для каждого свойства, возвращаемого в *папарам*, элемент **nзначения** указывает количество структур [**Декстер \_ значений**](dexter-value.md) , связанных со свойством.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-119">For each property returned in *paParam*, the **nValues** member indicates the number of [**DEXTER\_VALUE**](dexter-value.md) structures associated with the property.</span></span> <span data-ttu-id="1ec6c-120">Эти пары возвращаются в возрастающем порядке по времени для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-120">The pairs are returned in ascending time order for each property.</span></span>

<span data-ttu-id="1ec6c-121">По завершении использования возвращенных структур вызовите метод [**ипропертисеттер:: фрипропс**](ipropertysetter-freeprops.md) , чтобы освободить ресурсы, выделенные этим методом.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-121">When you are finished using the returned structures, call [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) to free the resources allocated by this method.</span></span>

> [!Note]  
> <span data-ttu-id="1ec6c-122">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="1ec6c-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="1ec6c-123">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="1ec6c-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="1ec6c-124">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="1ec6c-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="1ec6c-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="1ec6c-125">Examples</span></span>

<span data-ttu-id="1ec6c-126">В следующем примере кода показано, как выполнить итерацию всех значений в экземпляре метода задания свойства:</span><span class="sxs-lookup"><span data-stu-id="1ec6c-126">The following code example shows how to iterate through all the values on an instance of the property setter:</span></span>


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a><span data-ttu-id="1ec6c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1ec6c-127">Requirements</span></span>



| <span data-ttu-id="1ec6c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1ec6c-128">Requirement</span></span> | <span data-ttu-id="1ec6c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1ec6c-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec6c-130">Header</span><span class="sxs-lookup"><span data-stu-id="1ec6c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1ec6c-131"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ec6c-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="1ec6c-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1ec6c-132">Library</span></span><br/> | <dl> <span data-ttu-id="1ec6c-133"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ec6c-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ec6c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ec6c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec6c-135">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="1ec6c-135">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="1ec6c-136">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="1ec6c-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




