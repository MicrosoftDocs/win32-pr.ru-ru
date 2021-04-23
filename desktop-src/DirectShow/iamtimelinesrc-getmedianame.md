---
description: Метод Жетмедианаме извлекает имя исходного файла, представленного этим исходным объектом.
ms.assetid: 6f468628-10e1-4746-9c3a-6dae9aa3f6ad
title: 'Метод Иамтимелинесрк:: Жетмедианаме (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3727d57371e5c7bab4f9d693a247b6b62a3ada17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674844"
---
# <a name="iamtimelinesrcgetmedianame-method"></a><span data-ttu-id="0d335-103">Метод Иамтимелинесрк:: Жетмедианаме</span><span class="sxs-lookup"><span data-stu-id="0d335-103">IAMTimelineSrc::GetMediaName method</span></span>

> [!Note]  
> <span data-ttu-id="0d335-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="0d335-104">\[Deprecated.</span></span> <span data-ttu-id="0d335-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d335-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d335-106">`GetMediaName`Метод получает имя исходного файла, представленного этим исходным объектом.</span><span class="sxs-lookup"><span data-stu-id="0d335-106">The `GetMediaName` method retrieves the name of the source file represented by this source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d335-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d335-107">Syntax</span></span>


```C++
HRESULT GetMediaName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="0d335-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d335-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d335-109">*Pval* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0d335-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0d335-110">Получает имя файла.</span><span class="sxs-lookup"><span data-stu-id="0d335-110">Receives the name of the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d335-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d335-111">Return value</span></span>

<span data-ttu-id="0d335-112">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="0d335-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0d335-113">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d335-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d335-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d335-114">Remarks</span></span>

<span data-ttu-id="0d335-115">Метод выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="0d335-115">The method allocates memory for the string.</span></span> <span data-ttu-id="0d335-116">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="0d335-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="0d335-117">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="0d335-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="0d335-118">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0d335-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="0d335-119">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="0d335-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d335-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0d335-120">Requirements</span></span>



| <span data-ttu-id="0d335-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0d335-121">Requirement</span></span> | <span data-ttu-id="0d335-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0d335-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d335-123">Header</span><span class="sxs-lookup"><span data-stu-id="0d335-123">Header</span></span><br/>  | <dl> <span data-ttu-id="0d335-124"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d335-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="0d335-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d335-125">Library</span></span><br/> | <dl> <span data-ttu-id="0d335-126"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d335-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d335-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d335-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d335-128">**Интерфейс Иамтимелинесрк**</span><span class="sxs-lookup"><span data-stu-id="0d335-128">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="0d335-129">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="0d335-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




