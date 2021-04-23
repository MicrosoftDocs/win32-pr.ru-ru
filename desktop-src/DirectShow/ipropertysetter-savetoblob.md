---
description: Метод Саветоблоб сохраняет данные свойств в формате сохраняемости.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: 'Метод Ипропертисеттер:: Саветоблоб (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 97e248ebf741b45e73c82b17eee4181b1f19ac35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675805"
---
# <a name="ipropertysettersavetoblob-method"></a><span data-ttu-id="03bea-103">Метод Ипропертисеттер:: Саветоблоб</span><span class="sxs-lookup"><span data-stu-id="03bea-103">IPropertySetter::SaveToBlob method</span></span>

> [!Note]  
> <span data-ttu-id="03bea-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="03bea-104">\[Deprecated.</span></span> <span data-ttu-id="03bea-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03bea-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="03bea-106">`SaveToBlob`Метод сохраняет данные свойства в формате сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="03bea-106">The `SaveToBlob` method saves the property data to a persistence format.</span></span>

## <a name="syntax"></a><span data-ttu-id="03bea-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03bea-107">Syntax</span></span>


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a><span data-ttu-id="03bea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="03bea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03bea-109">*пксизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="03bea-109">*pcSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03bea-110">Получает размер данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="03bea-110">Receives the size of the data, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="03bea-111">*ППБ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="03bea-111">*ppb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03bea-112">Получает указатель на массив байтов, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="03bea-112">Receives a pointer to an array of bytes that receives the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03bea-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03bea-113">Return value</span></span>

<span data-ttu-id="03bea-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="03bea-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03bea-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03bea-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="03bea-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03bea-116">Remarks</span></span>

<span data-ttu-id="03bea-117">Метод выделяет память для массива байтов.</span><span class="sxs-lookup"><span data-stu-id="03bea-117">The method allocates memory for the byte array.</span></span> <span data-ttu-id="03bea-118">Вызывающий объект должен освободить его с помощью функции **CoTaskMemFree** .</span><span class="sxs-lookup"><span data-stu-id="03bea-118">The caller must free it, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="03bea-119">Все имена и значения свойств усекаются до 40 символов.</span><span class="sxs-lookup"><span data-stu-id="03bea-119">All property names and values are truncated to 40 characters in length.</span></span> <span data-ttu-id="03bea-120">По этой причине XML является предпочтительным форматом сохраняемости.</span><span class="sxs-lookup"><span data-stu-id="03bea-120">For this reason, XML is the preferred persistence format.</span></span> <span data-ttu-id="03bea-121">См. раздел [**интерфейс IXml2Dex**](ixml2dex.md).</span><span class="sxs-lookup"><span data-stu-id="03bea-121">See [**IXml2Dex Interface**](ixml2dex.md).</span></span>

> [!Note]  
> <span data-ttu-id="03bea-122">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="03bea-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="03bea-123">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="03bea-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="03bea-124">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="03bea-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03bea-125">Требования</span><span class="sxs-lookup"><span data-stu-id="03bea-125">Requirements</span></span>



| <span data-ttu-id="03bea-126">Требование</span><span class="sxs-lookup"><span data-stu-id="03bea-126">Requirement</span></span> | <span data-ttu-id="03bea-127">Значение</span><span class="sxs-lookup"><span data-stu-id="03bea-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="03bea-128">Header</span><span class="sxs-lookup"><span data-stu-id="03bea-128">Header</span></span><br/>  | <dl> <span data-ttu-id="03bea-129"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="03bea-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="03bea-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03bea-130">Library</span></span><br/> | <dl> <span data-ttu-id="03bea-131"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03bea-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03bea-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03bea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03bea-133">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="03bea-133">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="03bea-134">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="03bea-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




