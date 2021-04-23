---
title: Идврителокалфонтфилелоадер Жетфилепасфромкэй, метод
description: Получает абсолютный путь к файлу шрифта из ключа ссылки на файл шрифта.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Непосредственная запись метода Жетфилепасфромкэй
- Прямая запись метода Жетфилепасфромкэй, интерфейс Идврителокалфонтфилелоадер
- Прямая запись интерфейса Идврителокалфонтфилелоадер, метод Жетфилепасфромкэй
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688938"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a><span data-ttu-id="8fcb7-106">Метод Идврителокалфонтфилелоадер:: Жетфилепасфромкэй</span><span class="sxs-lookup"><span data-stu-id="8fcb7-106">IDWriteLocalFontFileLoader::GetFilePathFromKey method</span></span>

<span data-ttu-id="8fcb7-107">Получает абсолютный путь к файлу шрифта из ключа ссылки на файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="8fcb7-107">Obtains the absolute font file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fcb7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fcb7-108">Syntax</span></span>


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8fcb7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fcb7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fcb7-110">*фонтфилереференцекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8fcb7-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcb7-111">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="8fcb7-111">Type: **const void\***</span></span>

<span data-ttu-id="8fcb7-112">Ключ ссылки на файл шрифта, однозначно определяющий файл локального шрифта в пределах используемого загрузчика шрифтов.</span><span class="sxs-lookup"><span data-stu-id="8fcb7-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="8fcb7-113">*фонтфилереференцекэйсизе*</span><span class="sxs-lookup"><span data-stu-id="8fcb7-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="8fcb7-114">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8fcb7-114">Type: **UINT32**</span></span>

<span data-ttu-id="8fcb7-115">Размер ключа ссылки на файл шрифта в байтах.</span><span class="sxs-lookup"><span data-stu-id="8fcb7-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="8fcb7-116">*путь к файлу* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8fcb7-116">*filePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fcb7-117">Тип: **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="8fcb7-117">Type: **WCHAR\***</span></span>

<span data-ttu-id="8fcb7-118">Массив символов, который получает путь к локальному файлу.</span><span class="sxs-lookup"><span data-stu-id="8fcb7-118">The character array that receives the local file path.</span></span>

</dd> <dt>

<span data-ttu-id="8fcb7-119">*филепассизе*</span><span class="sxs-lookup"><span data-stu-id="8fcb7-119">*filePathSize*</span></span> 
</dt> <dd>

<span data-ttu-id="8fcb7-120">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8fcb7-120">Type: **UINT32**</span></span>

<span data-ttu-id="8fcb7-121">Длина массива символов пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="8fcb7-121">The length of the file path character array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fcb7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fcb7-122">Return value</span></span>

<span data-ttu-id="8fcb7-123">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8fcb7-123">Type: **HRESULT**</span></span>

<span data-ttu-id="8fcb7-124">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="8fcb7-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8fcb7-125">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8fcb7-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fcb7-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8fcb7-126">Requirements</span></span>



| <span data-ttu-id="8fcb7-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8fcb7-127">Requirement</span></span> | <span data-ttu-id="8fcb7-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8fcb7-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcb7-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8fcb7-129">Library</span></span><br/> | <dl> <span data-ttu-id="8fcb7-130"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fcb7-130"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="8fcb7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8fcb7-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="8fcb7-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fcb7-132"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fcb7-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fcb7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcb7-134">**идврителокалфонтфилелоадер**</span><span class="sxs-lookup"><span data-stu-id="8fcb7-134">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





