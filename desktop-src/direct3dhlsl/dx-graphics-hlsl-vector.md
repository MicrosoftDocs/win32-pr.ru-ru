---
title: Тип вектора (HLSL)
description: Вектор содержит от одного до четырех скалярных компонентов; Каждый компонент вектора должен иметь один и тот же тип.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Тип вектора HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "104997998"
---
# <a name="vector-type"></a><span data-ttu-id="5ef9a-104">Тип вектора</span><span class="sxs-lookup"><span data-stu-id="5ef9a-104">Vector Type</span></span>

<span data-ttu-id="5ef9a-105">Вектор содержит от одного до четырех скалярных компонентов; Каждый компонент вектора должен иметь один и тот же тип.</span><span class="sxs-lookup"><span data-stu-id="5ef9a-105">A vector contains between one and four scalar components; every component of a vector must be of the same type.</span></span>



|                     |
|---------------------|
| <span data-ttu-id="5ef9a-106">**Имя Типенумбер**</span><span class="sxs-lookup"><span data-stu-id="5ef9a-106">**TypeNumber Name**</span></span> |



 


```
TypeComponents Name
```



## <a name="components"></a><span data-ttu-id="5ef9a-107">Компоненты</span><span class="sxs-lookup"><span data-stu-id="5ef9a-107">Components</span></span>



| <span data-ttu-id="5ef9a-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="5ef9a-108">Item</span></span>                                                                                                                             | <span data-ttu-id="5ef9a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5ef9a-109">Description</span></span>                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef9a-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**типекомпонентс**</span><span class="sxs-lookup"><span data-stu-id="5ef9a-110"><span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**</span></span><br/> | <span data-ttu-id="5ef9a-111">Одно имя, содержащее две части.</span><span class="sxs-lookup"><span data-stu-id="5ef9a-111">A single name that contains two parts.</span></span> <span data-ttu-id="5ef9a-112">Первая часть является одним из [скалярных](dx-graphics-hlsl-data-types.md) типов.</span><span class="sxs-lookup"><span data-stu-id="5ef9a-112">The first part is one of the [scalar](dx-graphics-hlsl-data-types.md) types.</span></span> <span data-ttu-id="5ef9a-113">Вторая часть — это число компонентов, которое должно находиться в диапазоне от 1 до 4 включительно.</span><span class="sxs-lookup"><span data-stu-id="5ef9a-113">The second part is the number of components, which must be between 1 and 4 inclusive.</span></span><br/> |
| <span data-ttu-id="5ef9a-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Безымян**</span><span class="sxs-lookup"><span data-stu-id="5ef9a-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/>                                         | <span data-ttu-id="5ef9a-115">Строка ASCII, однозначно определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="5ef9a-115">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                |



 

## <a name="examples"></a><span data-ttu-id="5ef9a-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="5ef9a-116">Examples</span></span>

<span data-ttu-id="5ef9a-117">Ниже приводится несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="5ef9a-117">Here are some examples:</span></span>


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



<span data-ttu-id="5ef9a-118">Вектор можно объявить с помощью этого синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="5ef9a-118">A vector can be declared using this syntax also:</span></span>


```
vector <Type, Number> VariableName
```



<span data-ttu-id="5ef9a-119">Ниже приводится несколько примеров.</span><span class="sxs-lookup"><span data-stu-id="5ef9a-119">Here are some examples:</span></span>


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a><span data-ttu-id="5ef9a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ef9a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef9a-121">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5ef9a-121">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





