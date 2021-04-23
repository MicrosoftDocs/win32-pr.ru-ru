---
title: Функция Глужетстринг (GLU. h)
description: Функция Глужетстринг возвращает строку, описывающую номер версии GLU или поддерживаемые вызовы расширения GLU.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- Функция Глужетстринг OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415336"
---
# <a name="glugetstring-function"></a><span data-ttu-id="55f9f-104">Функция Глужетстринг</span><span class="sxs-lookup"><span data-stu-id="55f9f-104">gluGetString function</span></span>

<span data-ttu-id="55f9f-105">Функция **глужетстринг** возвращает строку, описывающую номер версии Glu или поддерживаемые вызовы расширения Glu.</span><span class="sxs-lookup"><span data-stu-id="55f9f-105">The **gluGetString** function gets a string that describes the GLU version number or supported GLU extension calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f9f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55f9f-106">Syntax</span></span>


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="55f9f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="55f9f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55f9f-108">*name*</span><span class="sxs-lookup"><span data-stu-id="55f9f-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="55f9f-109">Номер версии GLU ( \_ версия GLU) или доступные вызовы расширения для конкретного поставщика ( \_ расширения GLU).</span><span class="sxs-lookup"><span data-stu-id="55f9f-109">Either the version number of GLU (GLU\_VERSION) or available vendor-specific extension calls (GLU\_EXTENSIONS).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55f9f-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55f9f-110">Remarks</span></span>

<span data-ttu-id="55f9f-111">Функция **глужетстринг** возвращает указатель на статическую строку, завершающуюся нулем.</span><span class="sxs-lookup"><span data-stu-id="55f9f-111">The **gluGetString** function returns a pointer to a static, null-terminated string.</span></span> <span data-ttu-id="55f9f-112">Если *Name* — Glu \_ Version, возвращаемая строка представляет собой значение, представляющее номер версии Glu.</span><span class="sxs-lookup"><span data-stu-id="55f9f-112">When *name* is GLU\_VERSION, the returned string is a value that represents the version number of GLU.</span></span> <span data-ttu-id="55f9f-113">Формат номера версии выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55f9f-113">The format of the version number is as follows:</span></span>

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

<span data-ttu-id="55f9f-114">Номер версии имеет формат "основной \_ номер. дополнительный \_ номер" или "основной номер. \_ дополнительный номер \_ . \_ номер выпуска".</span><span class="sxs-lookup"><span data-stu-id="55f9f-114">The version number has the form "major\_number.minor\_number" or "major\_number.minor\_number.release\_number".</span></span> <span data-ttu-id="55f9f-115">Сведения, относящиеся к поставщику, являются необязательными, а формат и содержимое зависят от реализации.</span><span class="sxs-lookup"><span data-stu-id="55f9f-115">The vendor-specific information is optional, and the format and contents depend on the implementation.</span></span>

<span data-ttu-id="55f9f-116">Если *Name* — Glu \_ Extensions, возвращаемая строка содержит список имен поддерживаемых расширений Glu, разделенных пробелами.</span><span class="sxs-lookup"><span data-stu-id="55f9f-116">When *name* is GLU\_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces.</span></span> <span data-ttu-id="55f9f-117">Формат возвращаемого списка имен выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="55f9f-117">The format of the returned list of names is as follows:</span></span>

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

<span data-ttu-id="55f9f-118">Имена расширений не могут содержать пробелы.</span><span class="sxs-lookup"><span data-stu-id="55f9f-118">The extension names cannot contain any spaces.</span></span>

<span data-ttu-id="55f9f-119">Функция **глужетстринг** допустима для GLU версии 1,1 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="55f9f-119">The **gluGetString** function is valid for GLU version 1.1 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f9f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="55f9f-120">Requirements</span></span>



| <span data-ttu-id="55f9f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="55f9f-121">Requirement</span></span> | <span data-ttu-id="55f9f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="55f9f-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55f9f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55f9f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="55f9f-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55f9f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="55f9f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55f9f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="55f9f-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55f9f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55f9f-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="55f9f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="55f9f-128"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="55f9f-128"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="55f9f-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55f9f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="55f9f-130"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55f9f-130"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="55f9f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="55f9f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55f9f-132"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55f9f-132"><dt>Glu32.dll</dt></span></span> </dl> |



 

 





