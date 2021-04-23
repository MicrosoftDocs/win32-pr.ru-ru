---
description: Метод Жетвендорстринг извлекает имя поставщика. Для объектов модуля подготовки отчетов, предоставляемых DirectShow, строка поставщика имеет значение &\# 0034; Корпорация Майкрософт&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'Метод Ирендеренгине:: Жетвендорстринг (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676031"
---
# <a name="irenderenginegetvendorstring-method"></a><span data-ttu-id="80868-104">Метод Ирендеренгине:: Жетвендорстринг</span><span class="sxs-lookup"><span data-stu-id="80868-104">IRenderEngine::GetVendorString method</span></span>

> [!Note]  
> <span data-ttu-id="80868-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="80868-105">\[Deprecated.</span></span> <span data-ttu-id="80868-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="80868-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="80868-107">`GetVendorString`Метод извлекает имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="80868-107">The `GetVendorString` method retrieves the name of the vendor.</span></span> <span data-ttu-id="80868-108">Для объектов модуля подготовки отчетов, предоставляемых DirectShow, строка поставщика имеет значение «Корпорация Майкрософт».</span><span class="sxs-lookup"><span data-stu-id="80868-108">For the render engine objects that are provided by DirectShow, the vendor string is "Microsoft Corporation".</span></span>

## <a name="syntax"></a><span data-ttu-id="80868-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80868-109">Syntax</span></span>


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a><span data-ttu-id="80868-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="80868-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80868-111">*пвендорид* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="80868-111">*pVendorID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="80868-112">Получает **BSTR** , содержащий строку поставщика.</span><span class="sxs-lookup"><span data-stu-id="80868-112">Receives a **BSTR** containing the vendor string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80868-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80868-113">Return value</span></span>

<span data-ttu-id="80868-114">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="80868-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80868-115">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80868-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="80868-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80868-116">Remarks</span></span>

<span data-ttu-id="80868-117">Метод выделяет память для строки.</span><span class="sxs-lookup"><span data-stu-id="80868-117">The method allocates memory for the string.</span></span> <span data-ttu-id="80868-118">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="80868-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="80868-119">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="80868-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="80868-120">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="80868-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="80868-121">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="80868-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80868-122">Требования</span><span class="sxs-lookup"><span data-stu-id="80868-122">Requirements</span></span>



| <span data-ttu-id="80868-123">Требование</span><span class="sxs-lookup"><span data-stu-id="80868-123">Requirement</span></span> | <span data-ttu-id="80868-124">Значение</span><span class="sxs-lookup"><span data-stu-id="80868-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80868-125">Header</span><span class="sxs-lookup"><span data-stu-id="80868-125">Header</span></span><br/>  | <dl> <span data-ttu-id="80868-126"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="80868-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="80868-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="80868-127">Library</span></span><br/> | <dl> <span data-ttu-id="80868-128"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80868-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80868-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80868-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80868-130">**Интерфейс Ирендеренгине**</span><span class="sxs-lookup"><span data-stu-id="80868-130">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="80868-131">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="80868-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




