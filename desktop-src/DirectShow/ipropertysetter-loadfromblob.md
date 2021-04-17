---
description: Метод Лоадфромблоб загружает данные свойств из формата сохраняемости.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'Метод Ипропертисеттер:: Лоадфромблоб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0a1e58aa5802e8fcb05c2464fc1f121ee1e86f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675024"
---
# <a name="ipropertysetterloadfromblob-method"></a><span data-ttu-id="c6441-103">Метод Ипропертисеттер:: Лоадфромблоб</span><span class="sxs-lookup"><span data-stu-id="c6441-103">IPropertySetter::LoadFromBlob method</span></span>

> [!Note]  
> <span data-ttu-id="c6441-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c6441-104">\[Deprecated.</span></span> <span data-ttu-id="c6441-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c6441-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c6441-106">`LoadFromBlob`Метод загружает данные свойств из формата сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="c6441-106">The `LoadFromBlob` method loads property data from a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6441-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6441-107">Syntax</span></span>


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a><span data-ttu-id="c6441-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6441-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6441-109">*ксизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6441-109">*cSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6441-110">Размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="c6441-110">Size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c6441-111">*Pb* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6441-111">*pb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6441-112">Указатель на массив байтов, который содержит данные.</span><span class="sxs-lookup"><span data-stu-id="c6441-112">Pointer to an array of bytes that contains the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6441-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6441-113">Return value</span></span>

<span data-ttu-id="c6441-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c6441-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c6441-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c6441-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6441-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6441-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c6441-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="c6441-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c6441-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c6441-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c6441-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="c6441-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6441-120">Требования</span><span class="sxs-lookup"><span data-stu-id="c6441-120">Requirements</span></span>



| <span data-ttu-id="c6441-121">Требование</span><span class="sxs-lookup"><span data-stu-id="c6441-121">Requirement</span></span> | <span data-ttu-id="c6441-122">Значение</span><span class="sxs-lookup"><span data-stu-id="c6441-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6441-123">Header</span><span class="sxs-lookup"><span data-stu-id="c6441-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c6441-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6441-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c6441-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c6441-125">Library</span></span><br/> | <dl> <span data-ttu-id="c6441-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c6441-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6441-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6441-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6441-128">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="c6441-128">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="c6441-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="c6441-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




