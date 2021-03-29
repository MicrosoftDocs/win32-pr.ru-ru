---
title: Класс Matrix4x3F (D2d1 \_ Helper. h)
description: Класс Matrix4x3F представляет матрицу 4 на 3 и предоставляет удобные методы для создания матриц.
ms.assetid: 633B1828-0CB5-4CD3-9826-C65083C6C0A9
keywords:
- Класс Matrix4x3F Direct2D
- Matrix4x3F класс Direct2D, описание
topic_type:
- apiref
api_name:
- Matrix4x3F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81467b51eb22586d537c7ea8032e13a30da19c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892766"
---
# <a name="matrix4x3f-class"></a><span data-ttu-id="2b3e0-105">Класс Matrix4x3F</span><span class="sxs-lookup"><span data-stu-id="2b3e0-105">Matrix4x3F class</span></span>

<span data-ttu-id="2b3e0-106">Класс **Matrix4x3F** представляет матрицу 4 на 3 и предоставляет удобные методы для создания матриц.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-106">The **Matrix4x3F** class represents a 4-by-3 matrix and provides convenience methods for creating matrices.</span></span>

## <a name="members"></a><span data-ttu-id="2b3e0-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2b3e0-107">Members</span></span>

<span data-ttu-id="2b3e0-108">Класс **Matrix4x3F** наследует от [**D2D1 \_ Matrix \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span><span class="sxs-lookup"><span data-stu-id="2b3e0-108">The **Matrix4x3F** class inherits from [**D2D1\_MATRIX\_4X3\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span></span> <span data-ttu-id="2b3e0-109">**Matrix4x3F** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2b3e0-109">**Matrix4x3F** also has these types of members:</span></span>

-   [<span data-ttu-id="2b3e0-110">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="2b3e0-110">Constructors</span></span>](#constructors)

### <a name="constructors"></a><span data-ttu-id="2b3e0-111">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="2b3e0-111">Constructors</span></span>

<span data-ttu-id="2b3e0-112">Класс **Matrix4x3F** содержит эти конструкторы.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-112">The **Matrix4x3F** class has these constructors.</span></span>



| <span data-ttu-id="2b3e0-113">Конструктор</span><span class="sxs-lookup"><span data-stu-id="2b3e0-113">Constructor</span></span>                                                                                                                                                                                           | <span data-ttu-id="2b3e0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2b3e0-114">Description</span></span>                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b3e0-115">**Matrix4x3F()**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-115">**Matrix4x3F()**</span></span>](matrix4x3f-matrix4x3f--.md)                                                                                                                                                       | <span data-ttu-id="2b3e0-116">Создает новый экземпляр неинициализированного класса **Matrix4x3F** .</span><span class="sxs-lookup"><span data-stu-id="2b3e0-116">Instantiates a new instance of an uninitialized **Matrix4x3F** class.</span></span><br/>                                                   |
| [<span data-ttu-id="2b3e0-117">**Matrix4x3F (FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, float, float, float, float) (FLOAT, FLOAT, float, float, FLOAT, FLOAT, float, float, FLOAT, FLOAT, float, float)**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-117">**Matrix4x3F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)**</span></span>](matrix4x3f-matrix4x3f-floats-.md) | <span data-ttu-id="2b3e0-118">Создает новый экземпляр класса **Matrix4x3F** , инициализируемый всеми значениями матрицы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="2b3e0-118">Instantiates a new instance of a **Matrix4x3F** class that is initialized with all of the floating point matrix values.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b3e0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="2b3e0-119">Requirements</span></span>



| <span data-ttu-id="2b3e0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="2b3e0-120">Requirement</span></span> | <span data-ttu-id="2b3e0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="2b3e0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b3e0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b3e0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2b3e0-123">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="2b3e0-123">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="2b3e0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b3e0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2b3e0-125">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2b3e0-125">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="2b3e0-126">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="2b3e0-126">Minimum supported phone</span></span><br/>  | <span data-ttu-id="2b3e0-127">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b3e0-127">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="2b3e0-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b3e0-128">Namespace</span></span><br/>                | <span data-ttu-id="2b3e0-129">D2D1</span><span class="sxs-lookup"><span data-stu-id="2b3e0-129">D2D1</span></span><br/>                                                                                                                          |
| <span data-ttu-id="2b3e0-130">Header</span><span class="sxs-lookup"><span data-stu-id="2b3e0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b3e0-131"><dt>\_Вспомогательный метод D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e0-131"><dt>D2d1\_helper.h</dt></span></span> </dl>                                                |
| <span data-ttu-id="2b3e0-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2b3e0-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b3e0-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e0-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="2b3e0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2b3e0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b3e0-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b3e0-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



## <a name="see-also"></a><span data-ttu-id="2b3e0-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b3e0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b3e0-137">**D2D1 \_ Матрица \_ 4X3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="2b3e0-137">**D2D1\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)
</dt> </dl>

 

 





