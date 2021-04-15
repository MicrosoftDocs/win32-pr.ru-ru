---
description: Содержит сведения о базовом модуле.
ms.assetid: 5cdb0b11-8bd3-46d2-b214-85cdb2f274a7
title: Структура AUX_MODULE_BASIC_INFO (AUX \_ клиб. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AUX_MODULE_BASIC_INFO
api_type:
- HeaderDef
api_location:
- Aux_klib.h
ms.openlocfilehash: 1ee7300ec2c2d84e1ddadc4149135dab53d2336b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648881"
---
# <a name="aux_module_basic_info-structure"></a><span data-ttu-id="2e629-103">\_ \_ Основная \_ информационная структура модуля AUX</span><span class="sxs-lookup"><span data-stu-id="2e629-103">AUX\_MODULE\_BASIC\_INFO structure</span></span>

<span data-ttu-id="2e629-104">Содержит сведения о базовом модуле.</span><span class="sxs-lookup"><span data-stu-id="2e629-104">Contains basic module information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e629-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e629-105">Syntax</span></span>


```C++
typedef struct _AUX_MODULE_BASIC_INFO {
  PVOID ImageBase;
} AUX_MODULE_BASIC_INFO, *PAUX_MODULE_BASIC_INFO;
```



## <a name="members"></a><span data-ttu-id="2e629-106">Члены</span><span class="sxs-lookup"><span data-stu-id="2e629-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2e629-107">**ImageBase**</span><span class="sxs-lookup"><span data-stu-id="2e629-107">**ImageBase**</span></span>
</dt> <dd>

<span data-ttu-id="2e629-108">Базовый адрес модуля в адресном пространстве ядра.</span><span class="sxs-lookup"><span data-stu-id="2e629-108">The base address of the module within the kernel's address space.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e629-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2e629-109">Remarks</span></span>

<span data-ttu-id="2e629-110">Библиотеку объектов, реализующих этот API, можно скачать [отсюда](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="2e629-110">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="2e629-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2e629-111">Requirements</span></span>



| <span data-ttu-id="2e629-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2e629-112">Requirement</span></span> | <span data-ttu-id="2e629-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2e629-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e629-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2e629-114">Redistributable</span></span><br/> | <span data-ttu-id="2e629-115">Библиотека вспомогательных API Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="2e629-115">Windows Auxiliary API library version 1.0 or later</span></span><br/>                          |
| <span data-ttu-id="2e629-116">Header</span><span class="sxs-lookup"><span data-stu-id="2e629-116">Header</span></span><br/>          | <dl> <span data-ttu-id="2e629-117"><dt>AUX \_ клиб. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e629-117"><dt>Aux\_klib.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e629-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2e629-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e629-119">**ауксклибкуеримодулеинформатион**</span><span class="sxs-lookup"><span data-stu-id="2e629-119">**AuxKlibQueryModuleInformation**</span></span>](auxklibquerymoduleinformation-func.md)
</dt> </dl>

 

 




