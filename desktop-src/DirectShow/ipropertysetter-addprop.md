---
description: Метод Аддпроп добавляет свойство в установщик свойств с массивом пар "время — значение", определяющим значение свойства за определенный период времени.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Метод Ипропертисеттер:: Аддпроп (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675027"
---
# <a name="ipropertysetteraddprop-method"></a><span data-ttu-id="7d63a-103">Метод Ипропертисеттер:: Аддпроп</span><span class="sxs-lookup"><span data-stu-id="7d63a-103">IPropertySetter::AddProp method</span></span>

> [!Note]  
> <span data-ttu-id="7d63a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="7d63a-104">\[Deprecated.</span></span> <span data-ttu-id="7d63a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7d63a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7d63a-106">`AddProp`Метод добавляет свойство в установщик свойств с массивом пар "время — значение", определяющим значение свойства за определенный период времени.</span><span class="sxs-lookup"><span data-stu-id="7d63a-106">The `AddProp` method adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d63a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d63a-107">Syntax</span></span>


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="7d63a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d63a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d63a-109">*Параметр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d63a-109">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d63a-110">[**Декстер \_ Структура PARAM**](dexter-param.md) , указывающая свойство.</span><span class="sxs-lookup"><span data-stu-id="7d63a-110">[**DEXTER\_PARAM**](dexter-param.md) structure that specifies the property.</span></span> <span data-ttu-id="7d63a-111">Элемент **nзначения** структуры должен равняться размеру массива, заданного в параметре *павалуе* .</span><span class="sxs-lookup"><span data-stu-id="7d63a-111">The **nValues** member of the structure must equal the size of the array given in the *paValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="7d63a-112">*павалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d63a-112">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d63a-113">Указатель на массив структур [**\_ значений Декстер**](dexter-value.md) , содержащих пары "время — значение".</span><span class="sxs-lookup"><span data-stu-id="7d63a-113">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures that contain time-value pairs.</span></span> <span data-ttu-id="7d63a-114">Массив должен быть в порядке возрастания времени.</span><span class="sxs-lookup"><span data-stu-id="7d63a-114">The array must be in ascending time order.</span></span> <span data-ttu-id="7d63a-115">Время задается относительно времени начала действия или перехода.</span><span class="sxs-lookup"><span data-stu-id="7d63a-115">The times are relative to the starting time of the effect or transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d63a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d63a-116">Return value</span></span>

<span data-ttu-id="7d63a-117">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="7d63a-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7d63a-118">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7d63a-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d63a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d63a-119">Remarks</span></span>

<span data-ttu-id="7d63a-120">Первая структура [**\_ значения Декстер**](dexter-value.md) должна задавать время ссылки, равное нулю, и флаг интерполяции (**двинтерп**) **\_ перехода декстерф** или метод возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="7d63a-120">The first [**DEXTER\_VALUE**](dexter-value.md) structure must specify a reference time of zero and an interpolation flag (**dwInterp**) of **DEXTERF\_JUMP**, or the method returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="7d63a-121">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="7d63a-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7d63a-122">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d63a-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7d63a-123">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="7d63a-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7d63a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="7d63a-124">Requirements</span></span>



| <span data-ttu-id="7d63a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="7d63a-125">Requirement</span></span> | <span data-ttu-id="7d63a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="7d63a-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d63a-127">Header</span><span class="sxs-lookup"><span data-stu-id="7d63a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="7d63a-128"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d63a-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7d63a-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="7d63a-129">Library</span></span><br/> | <dl> <span data-ttu-id="7d63a-130"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7d63a-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d63a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d63a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d63a-132">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="7d63a-132">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="7d63a-133">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="7d63a-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




