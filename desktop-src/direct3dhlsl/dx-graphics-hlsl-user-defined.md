---
title: Определяемый пользователем тип
description: Чтобы объявить определяемый пользователем тип, используйте следующий синтаксис.
ms.assetid: 8ef18864-f456-4b52-af83-f9b1050a0bba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2107e3eb2b2dc2362776a1a9ecd50830519c6627
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410746"
---
# <a name="user-defined-type"></a><span data-ttu-id="0b2dc-103">Определяемый пользователем тип</span><span class="sxs-lookup"><span data-stu-id="0b2dc-103">User-Defined Type</span></span>

<span data-ttu-id="0b2dc-104">Чтобы объявить определяемый пользователем тип, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-104">Use the following syntax to declare a user-defined type.</span></span>



|                                           |
|-------------------------------------------|
| <span data-ttu-id="0b2dc-105">typedef **\[ const \] имя типа \[ , \] индекс**;</span><span class="sxs-lookup"><span data-stu-id="0b2dc-105">typedef **\[const\] Type Name\[Index\]**;</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="0b2dc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b2dc-106">Parameters</span></span>



| <span data-ttu-id="0b2dc-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="0b2dc-107">Item</span></span>                                                                                         | <span data-ttu-id="0b2dc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0b2dc-108">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2dc-109"><span id="_const_"></span><span id="_CONST_"></span>**\[постоянного\]**</span><span class="sxs-lookup"><span data-stu-id="0b2dc-109"><span id="_const_"></span><span id="_CONST_"></span>**\[const\]**</span></span><br/>                 | <span data-ttu-id="0b2dc-110">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-110">Optional.</span></span> <span data-ttu-id="0b2dc-111">Это ключевое слово явно помечает тип как константу.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-111">This keyword explicitly marks the type as a constant.</span></span><br/>             |
| <span data-ttu-id="0b2dc-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Тип**</span><span class="sxs-lookup"><span data-stu-id="0b2dc-112"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/>     | <span data-ttu-id="0b2dc-113">Определяет тип данных; должен быть одним из встроенных типов данных HLSL.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-113">Identifies the data type; must be one of the HLSL intrinsic data types.</span></span><br/>     |
| <span data-ttu-id="0b2dc-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="0b2dc-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>     | <span data-ttu-id="0b2dc-115">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                 |
| <span data-ttu-id="0b2dc-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Номер**</span><span class="sxs-lookup"><span data-stu-id="0b2dc-116"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>**Index**</span></span><br/> | <span data-ttu-id="0b2dc-117">Необязательный размер массива.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-117">Optional array size.</span></span> <span data-ttu-id="0b2dc-118">Значение должно быть целым числом без знака от 1 до 4 включительно.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-118">Must be an unsigned integer between 1 and 4 inclusive.</span></span><br/> |



 

<span data-ttu-id="0b2dc-119">В дополнение к встроенным внутренним типам данных HLSL поддерживает определяемые пользователем или пользовательские типы, которые следуют этому синтаксису:</span><span class="sxs-lookup"><span data-stu-id="0b2dc-119">In addition to the built-in intrinsic data types, HLSL supports user-defined or custom types which follow this syntax:</span></span>

## <a name="remarks"></a><span data-ttu-id="0b2dc-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b2dc-120">Remarks</span></span>

<span data-ttu-id="0b2dc-121">В определяемых пользователем типах регистр символов не учитывается.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-121">User-defined types are not case-sensitive.</span></span> <span data-ttu-id="0b2dc-122">Для удобства следующие типы автоматически определяются в области супер-Глобальная.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-122">For convenience, the following types are automatically defined at super-global scope.</span></span>


```
typedef vector <bool, #> bool#;
typedef vector <int, #> int#;
typedef vector <uint, #> uint#;
typedef vector <half, #> half#;
typedef vector <float, #> float#;
typedef vector <double, #> double#;

typedef matrix <bool, #, #> bool#x#;
typedef matrix <int, #, #> int#x#;
typedef matrix <uint, #, #> uint#x#;
typedef matrix <half, #, #> half#x#;
typedef matrix <float, #, #> float#x#;
typedef matrix <double, #, #> double#x#;
```



<span data-ttu-id="0b2dc-123">Знак решетки ( \# ) представляет собой целую цифру от 1 до 4.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-123">The pound sign (\#) represents an integer digit between 1 and 4.</span></span>

<span data-ttu-id="0b2dc-124">Для совместимости с эффектами DirectX 8 следующие типы автоматически определяются в глобальной области.</span><span class="sxs-lookup"><span data-stu-id="0b2dc-124">For compatibility with DirectX 8 effects, the following types are automatically defined at super-global scope:</span></span>


```
typedef int DWORD;
typedef float FLOAT; 
typedef vector <float, 4> VECTOR;
typedef matrix <float, 4, 4> MATRIX;
typedef string STRING;
typedef texture TEXTURE;
typedef pixelshader PIXELSHADER;
typedef vertexshader VERTEXSHADER;
```



## <a name="related-topics"></a><span data-ttu-id="0b2dc-125">См. также</span><span class="sxs-lookup"><span data-stu-id="0b2dc-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b2dc-126">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0b2dc-126">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





