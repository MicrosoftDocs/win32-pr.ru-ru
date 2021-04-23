---
title: Идврителокалфонтфилелоадер Жетластвритетимефромкэй, метод
description: Получает время последней записи файла из ключа ссылки на файл шрифта.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Непосредственная запись метода Жетластвритетимефромкэй
- Прямая запись метода Жетластвритетимефромкэй, интерфейс Идврителокалфонтфилелоадер
- Прямая запись интерфейса Идврителокалфонтфилелоадер, метод Жетластвритетимефромкэй
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689025"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a><span data-ttu-id="c8ac6-106">Метод Идврителокалфонтфилелоадер:: Жетластвритетимефромкэй</span><span class="sxs-lookup"><span data-stu-id="c8ac6-106">IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey method</span></span>

<span data-ttu-id="c8ac6-107">Получает время последней записи файла из ключа ссылки на файл шрифта.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-107">Obtains the last write time of the file from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ac6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8ac6-108">Syntax</span></span>


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c8ac6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8ac6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ac6-110">*фонтфилереференцекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c8ac6-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ac6-111">Тип: **константа \* void**</span><span class="sxs-lookup"><span data-stu-id="c8ac6-111">Type: **const void\***</span></span>

<span data-ttu-id="c8ac6-112">Ключ ссылки на файл шрифта, однозначно определяющий файл локального шрифта в пределах используемого загрузчика шрифтов.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="c8ac6-113">*фонтфилереференцекэйсизе*</span><span class="sxs-lookup"><span data-stu-id="c8ac6-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="c8ac6-114">Тип: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c8ac6-114">Type: **UINT32**</span></span>

<span data-ttu-id="c8ac6-115">Размер ключа ссылки на файл шрифта в байтах.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="c8ac6-116">*LastWriteTime* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c8ac6-116">*lastWriteTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ac6-117">Тип: **fileTime \***</span><span class="sxs-lookup"><span data-stu-id="c8ac6-117">Type: **FILETIME\***</span></span>

<span data-ttu-id="c8ac6-118">Время последнего изменения файла шрифта.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-118">The time of the last font file modification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8ac6-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8ac6-119">Return value</span></span>

<span data-ttu-id="c8ac6-120">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c8ac6-120">Type: **HRESULT**</span></span>

<span data-ttu-id="c8ac6-121">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c8ac6-122">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c8ac6-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ac6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="c8ac6-123">Requirements</span></span>



| <span data-ttu-id="c8ac6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="c8ac6-124">Requirement</span></span> | <span data-ttu-id="c8ac6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="c8ac6-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ac6-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c8ac6-126">Library</span></span><br/> | <dl> <span data-ttu-id="c8ac6-127"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8ac6-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8ac6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c8ac6-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8ac6-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8ac6-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ac6-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8ac6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ac6-131">**идврителокалфонтфилелоадер**</span><span class="sxs-lookup"><span data-stu-id="c8ac6-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





