---
description: Метод Принтксмл преобразует данные свойств в XML-строку.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: 'Ипропертисеттер: метод:P Ринтксмл (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675807"
---
# <a name="ipropertysetterprintxml-method"></a><span data-ttu-id="ac4e6-103">Ипропертисеттер: метод:P Ринтксмл</span><span class="sxs-lookup"><span data-stu-id="ac4e6-103">IPropertySetter::PrintXML method</span></span>

> [!Note]  
> <span data-ttu-id="ac4e6-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-104">\[Deprecated.</span></span> <span data-ttu-id="ac4e6-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ac4e6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ac4e6-106">`PrintXML`Метод преобразует данные свойства в XML-строку.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-106">The `PrintXML` method converts property data into an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4e6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac4e6-107">Syntax</span></span>


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a><span data-ttu-id="ac4e6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac4e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac4e6-109">*псзксмл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac4e6-109">*pszXML* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4e6-110">Указатель на буфер, который получает XML-строку.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-110">Pointer to a buffer that receives the XML string.</span></span>

</dd> <dt>

<span data-ttu-id="ac4e6-111">*кбксмл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac4e6-111">*cbXML* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4e6-112">Размер буфера, на который указывает *псзксмл*, в байтах.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-112">Size of the buffer pointed to by *pszXML*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ac4e6-113">*пкбпринтед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ac4e6-113">*pcbPrinted* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4e6-114">Указатель на переменную, которая получает длину XML-строки.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-114">Pointer to a variable that receives the length of the XML string.</span></span> <span data-ttu-id="ac4e6-115">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ac4e6-116">*Отступ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ac4e6-116">*indent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4e6-117">Число уровней отступа для самого внешнего тега.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-117">Number of indent levels for the outermost tag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac4e6-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac4e6-118">Return value</span></span>

<span data-ttu-id="ac4e6-119">\_При успешном выполнении возвращает значение ОК.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-119">Returns S\_OK if successful.</span></span> <span data-ttu-id="ac4e6-120">В противном случае возвращает значение **HRESULT** , указывающее причину ошибки.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-120">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span> <span data-ttu-id="ac4e6-121">Если строка XML длиннее, чем буфер, метод возвращает E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-121">If the XML string is longer than the buffer, the method returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac4e6-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac4e6-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ac4e6-123">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="ac4e6-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ac4e6-124">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ac4e6-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ac4e6-125">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="ac4e6-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ac4e6-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ac4e6-126">Requirements</span></span>



| <span data-ttu-id="ac4e6-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ac4e6-127">Requirement</span></span> | <span data-ttu-id="ac4e6-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ac4e6-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ac4e6-129">Header</span><span class="sxs-lookup"><span data-stu-id="ac4e6-129">Header</span></span><br/>  | <dl> <span data-ttu-id="ac4e6-130"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac4e6-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ac4e6-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ac4e6-131">Library</span></span><br/> | <dl> <span data-ttu-id="ac4e6-132"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac4e6-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac4e6-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ac4e6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4e6-134">**Интерфейс Ипропертисеттер**</span><span class="sxs-lookup"><span data-stu-id="ac4e6-134">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="ac4e6-135">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="ac4e6-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




