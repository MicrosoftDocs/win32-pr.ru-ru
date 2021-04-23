---
title: IDWriteFactory2 Жетсистемфонтфаллбакк, метод
description: Создает резервный объект шрифта из списка резервных шрифтов системы.
ms.assetid: 7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420
keywords:
- Непосредственная запись метода Жетсистемфонтфаллбакк
- Прямая запись метода Жетсистемфонтфаллбакк, интерфейс IDWriteFactory2
- Прямая запись интерфейса IDWriteFactory2, метод Жетсистемфонтфаллбакк
topic_type:
- apiref
api_name:
- IDWriteFactory2.GetSystemFontFallback
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3f0eb73ee80dc3e6195267d25f6043225b8613ed
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413409"
---
# <a name="idwritefactory2getsystemfontfallback-method"></a><span data-ttu-id="ce6ff-106">Метод IDWriteFactory2:: Жетсистемфонтфаллбакк</span><span class="sxs-lookup"><span data-stu-id="ce6ff-106">IDWriteFactory2::GetSystemFontFallback method</span></span>

<span data-ttu-id="ce6ff-107">Создает резервный объект шрифта из списка резервных шрифтов системы.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-107">Creates a font fallback object from the system font fallback list.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce6ff-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce6ff-108">Syntax</span></span>


```C++
HRESULT GetSystemFontFallback(
  [out] IDWriteFontFallback **fontFallback
);
```



## <a name="parameters"></a><span data-ttu-id="ce6ff-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce6ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce6ff-110">*фонтфаллбакк* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ce6ff-110">*fontFallback* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce6ff-111">Тип: **[ **идвритефонтфаллбакк**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span><span class="sxs-lookup"><span data-stu-id="ce6ff-111">Type: **[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)\*\***</span></span>

<span data-ttu-id="ce6ff-112">Содержит адрес указателя на вновь созданный объект резервного шрифта.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-112">Contains an address of a pointer to the newly created font fallback object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce6ff-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce6ff-113">Return value</span></span>

<span data-ttu-id="ce6ff-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ce6ff-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ce6ff-115">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="ce6ff-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ce6ff-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ce6ff-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce6ff-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce6ff-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce6ff-118">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="ce6ff-118">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

 