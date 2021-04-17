---
title: IDWriteFont2 Исколорфонт, метод
description: Позволяет определить, является ли путь визуализации цвета потенциально необходимым.
ms.assetid: E21BB773-923E-461B-B966-A186ACD0164A
keywords:
- Непосредственная запись метода Исколорфонт
- Прямая запись метода Исколорфонт, интерфейс IDWriteFont2
- Прямая запись интерфейса IDWriteFont2, метод Исколорфонт
topic_type:
- apiref
api_name:
- IDWriteFont2.IsColorFont
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 353499c5e1c00ae37e585ecc6be47e5a2033d795
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415797"
---
# <a name="idwritefont2iscolorfont-method"></a><span data-ttu-id="1d528-106">Метод IDWriteFont2:: Исколорфонт</span><span class="sxs-lookup"><span data-stu-id="1d528-106">IDWriteFont2::IsColorFont method</span></span>

<span data-ttu-id="1d528-107">Позволяет определить, является ли путь визуализации цвета потенциально необходимым.</span><span class="sxs-lookup"><span data-stu-id="1d528-107">Enables determining if a color rendering path is potentially necessary.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d528-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d528-108">Syntax</span></span>


```C++
BOOL IsColorFont();
```



## <a name="parameters"></a><span data-ttu-id="1d528-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d528-109">Parameters</span></span>

<span data-ttu-id="1d528-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1d528-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d528-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d528-111">Return value</span></span>

<span data-ttu-id="1d528-112">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="1d528-112">Type: **BOOL**</span></span>

<span data-ttu-id="1d528-113">Возвращает **значение true** , если шрифт имеет сведения о цвете (таблицы КОЛР и кпал); в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="1d528-113">Returns **TRUE** if the font has color information (COLR and CPAL tables); otherwise **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d528-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1d528-114">Requirements</span></span>



| <span data-ttu-id="1d528-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1d528-115">Requirement</span></span> | <span data-ttu-id="1d528-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1d528-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d528-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d528-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d528-118">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="1d528-118">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="1d528-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d528-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d528-120">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="1d528-120">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="1d528-121">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="1d528-121">Minimum supported phone</span></span><br/>  | <span data-ttu-id="1d528-122">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="1d528-122">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="1d528-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1d528-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1d528-124"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d528-124"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1d528-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1d528-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d528-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d528-126"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1d528-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d528-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d528-128">**IDWriteFont2**</span><span class="sxs-lookup"><span data-stu-id="1d528-128">**IDWriteFont2**</span></span>](idwritefont2.md)
</dt> </dl>

 

 





