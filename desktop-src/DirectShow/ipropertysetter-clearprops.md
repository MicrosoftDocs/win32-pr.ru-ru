---
description: Метод Клеарпропс удаляет все данные свойств из метода задания свойств. Приложение может устанавливать новые данные свойств после вызова этой функции.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'Метод Ипропертисеттер:: Клеарпропс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675026"
---
# <a name="ipropertysetterclearprops-method"></a><span data-ttu-id="efc78-104">Метод Ипропертисеттер:: Клеарпропс</span><span class="sxs-lookup"><span data-stu-id="efc78-104">IPropertySetter::ClearProps method</span></span>

> [!Note]  
> <span data-ttu-id="efc78-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="efc78-105">\[Deprecated.</span></span> <span data-ttu-id="efc78-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="efc78-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="efc78-107">`ClearProps`Метод удаляет все данные свойств из метода задания свойств.</span><span class="sxs-lookup"><span data-stu-id="efc78-107">The `ClearProps` method clears all property data from the property setter.</span></span> <span data-ttu-id="efc78-108">Приложение может устанавливать новые данные свойств после вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="efc78-108">The application can set new property data after calling this function.</span></span>

<span data-ttu-id="efc78-109">Очистка данных свойства не приводит к восстановлению свойств объекта в исходных значениях.</span><span class="sxs-lookup"><span data-stu-id="efc78-109">Clearing the property data does not restore the object's properties to their original values.</span></span> <span data-ttu-id="efc78-110">Это просто предотвращает применение DirectShow дальнейших изменений.</span><span class="sxs-lookup"><span data-stu-id="efc78-110">It simply prevents DirectShow from applying any further changes.</span></span> <span data-ttu-id="efc78-111">Значения свойств применяются во время выполнения при отрисовке проекта.</span><span class="sxs-lookup"><span data-stu-id="efc78-111">Property values are applied at run time when the project renders.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc78-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efc78-112">Syntax</span></span>


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a><span data-ttu-id="efc78-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="efc78-113">Parameters</span></span>

<span data-ttu-id="efc78-114">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="efc78-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="efc78-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efc78-115">Return value</span></span>

<span data-ttu-id="efc78-116">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="efc78-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="efc78-117">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="efc78-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="efc78-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efc78-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="efc78-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="efc78-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="efc78-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="efc78-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="efc78-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="efc78-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="efc78-122">Требования</span><span class="sxs-lookup"><span data-stu-id="efc78-122">Requirements</span></span>



| <span data-ttu-id="efc78-123">Требование</span><span class="sxs-lookup"><span data-stu-id="efc78-123">Requirement</span></span> | <span data-ttu-id="efc78-124">Значение</span><span class="sxs-lookup"><span data-stu-id="efc78-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efc78-125">Header</span><span class="sxs-lookup"><span data-stu-id="efc78-125">Header</span></span><br/>  | <dl> <span data-ttu-id="efc78-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc78-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="efc78-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="efc78-127">Library</span></span><br/> | <dl> <span data-ttu-id="efc78-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efc78-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc78-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efc78-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc78-130">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="efc78-130">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="efc78-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="efc78-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




