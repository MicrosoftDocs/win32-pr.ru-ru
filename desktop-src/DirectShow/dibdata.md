---
description: Структура ДИБДАТА содержит сведения о аппаратно-независимом точечном рисунке (DIB) GDI.
ms.assetid: abbfa5b4-8789-4a44-a467-5812d3cc8238
title: Структура ДИБДАТА (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIBDATA
api_type:
- HeaderDef
api_location:
- Winutil.h
ms.openlocfilehash: 87590013ef905ffbdd13dd3b767435a907b08783
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105676001"
---
# <a name="dibdata-structure"></a><span data-ttu-id="9789c-103">Структура ДИБДАТА</span><span class="sxs-lookup"><span data-stu-id="9789c-103">DIBDATA structure</span></span>

<span data-ttu-id="9789c-104">`DIBDATA`Структура содержит сведения об аппаратно-независимом точечном рисунке GDI (DIB).</span><span class="sxs-lookup"><span data-stu-id="9789c-104">The `DIBDATA` structure contains information about a GDI device-independent bitmap (DIB).</span></span>

## <a name="syntax"></a><span data-ttu-id="9789c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9789c-105">Syntax</span></span>


```C++
typedef struct tagDIBDATA {
  LONG       PaletteVersion;
  DIBSECTION DibSection;
  HBITMAP    hBitmap;
  HANDLE     hMapping;
  BYTE       *pBase;
} DIBDATA;
```



## <a name="members"></a><span data-ttu-id="9789c-106">Члены</span><span class="sxs-lookup"><span data-stu-id="9789c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9789c-107">**палеттеверсион**</span><span class="sxs-lookup"><span data-stu-id="9789c-107">**PaletteVersion**</span></span>
</dt> <dd>

<span data-ttu-id="9789c-108">Этот элемент должен увеличиваться при каждом изменении палитры.</span><span class="sxs-lookup"><span data-stu-id="9789c-108">This member should be incremented whenever the palette changes.</span></span>

</dd> <dt>

<span data-ttu-id="9789c-109">**дибсектион**</span><span class="sxs-lookup"><span data-stu-id="9789c-109">**DibSection**</span></span>
</dt> <dd>

<span data-ttu-id="9789c-110">Структура **дибсектион** , содержащая сведения об элементе DIB.</span><span class="sxs-lookup"><span data-stu-id="9789c-110">**DIBSECTION** structure that contains information about the DIB.</span></span> <span data-ttu-id="9789c-111">Дополнительные сведения см. в документации по GDI.</span><span class="sxs-lookup"><span data-stu-id="9789c-111">See the GDI documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="9789c-112">**хбитмап**</span><span class="sxs-lookup"><span data-stu-id="9789c-112">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="9789c-113">Маркер для точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9789c-113">Handle to the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="9789c-114">**хмаппинг**</span><span class="sxs-lookup"><span data-stu-id="9789c-114">**hMapping**</span></span>
</dt> <dd>

<span data-ttu-id="9789c-115">Обрабатывает объект сопоставления файлов, используемый для совместного использования памяти между GDI и объектом [**Цимажесампле**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="9789c-115">Handle to a file-mapping object that is used to share memory between GDI and a [**CImageSample**](cimagesample.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="9789c-116">**pBase**</span><span class="sxs-lookup"><span data-stu-id="9789c-116">**pBase**</span></span>
</dt> <dd>

<span data-ttu-id="9789c-117">Адрес точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="9789c-117">Address of the bitmap.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9789c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9789c-118">Requirements</span></span>



| <span data-ttu-id="9789c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9789c-119">Requirement</span></span> | <span data-ttu-id="9789c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9789c-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9789c-121">Header</span><span class="sxs-lookup"><span data-stu-id="9789c-121">Header</span></span><br/> | <dl> <span data-ttu-id="9789c-122"><dt>Винутил. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9789c-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl> |



 

 




