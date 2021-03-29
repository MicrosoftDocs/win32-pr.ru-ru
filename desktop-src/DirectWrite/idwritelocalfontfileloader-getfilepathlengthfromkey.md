---
title: Идврителокалфонтфилелоадер Жетфилепасленгсфромкэй, метод
description: Получает длину абсолютного пути к файлу из ключа ссылки на файл шрифта.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Непосредственная запись метода Жетфилепасленгсфромкэй
- Прямая запись метода Жетфилепасленгсфромкэй, интерфейс Идврителокалфонтфилелоадер
- Прямая запись интерфейса Идврителокалфонтфилелоадер, метод Жетфилепасленгсфромкэй
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668876"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a><span data-ttu-id="1b3c0-106">Метод Идврителокалфонтфилелоадер:: Жетфилепасленгсфромкэй</span><span class="sxs-lookup"><span data-stu-id="1b3c0-106">IDWriteLocalFontFileLoader::GetFilePathLengthFromKey method</span></span>

<span data-ttu-id="1b3c0-107">Получает длину абсолютного пути к файлу из ключа ссылки на файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="1b3c0-107">Obtains the length of the absolute file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b3c0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b3c0-108">Syntax</span></span>


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a><span data-ttu-id="1b3c0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b3c0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b3c0-110">*фонтфилереференцекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1b3c0-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3c0-111">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="1b3c0-111">Type: **const void\***</span></span>

<span data-ttu-id="1b3c0-112">Ключ ссылки на файл шрифта, однозначно определяющий файл локального шрифта в области используемого загрузчика шрифтов.</span><span class="sxs-lookup"><span data-stu-id="1b3c0-112">Font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="1b3c0-113">*фонтфилереференцекэйсизе*</span><span class="sxs-lookup"><span data-stu-id="1b3c0-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="1b3c0-114">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="1b3c0-114">Type: **UINT32**</span></span>

<span data-ttu-id="1b3c0-115">Размер ключа ссылки на файл шрифта в байтах.</span><span class="sxs-lookup"><span data-stu-id="1b3c0-115">Size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1b3c0-116">*филепасленгс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1b3c0-116">*filePathLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3c0-117">Тип: **UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="1b3c0-117">Type: **UINT32\***</span></span>

<span data-ttu-id="1b3c0-118">Длина строки пути к файлу, не включая завершающий символ **null** .</span><span class="sxs-lookup"><span data-stu-id="1b3c0-118">Length of the file path string, not including the terminated **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b3c0-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1b3c0-119">Return value</span></span>

<span data-ttu-id="1b3c0-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1b3c0-120">Type: **HRESULT**</span></span>

<span data-ttu-id="1b3c0-121">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="1b3c0-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1b3c0-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1b3c0-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b3c0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="1b3c0-123">Requirements</span></span>



| <span data-ttu-id="1b3c0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="1b3c0-124">Requirement</span></span> | <span data-ttu-id="1b3c0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="1b3c0-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b3c0-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1b3c0-126">Library</span></span><br/> | <dl> <span data-ttu-id="1b3c0-127"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b3c0-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="1b3c0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1b3c0-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="1b3c0-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b3c0-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b3c0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b3c0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b3c0-131">**идврителокалфонтфилелоадер**</span><span class="sxs-lookup"><span data-stu-id="1b3c0-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





