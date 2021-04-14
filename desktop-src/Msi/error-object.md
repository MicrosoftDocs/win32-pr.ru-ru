---
description: Объект error Возвращает сведения об одной ошибке слияния.
ms.assetid: 38025e21-2d31-40f8-a088-2d3912c2893e
title: Объект Error (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error
- IMsmError
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 36fce310e6f75889ba5092f4fe43b6ca52ee2963
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651744"
---
# <a name="error-object"></a><span data-ttu-id="87284-103">Объект ошибки</span><span class="sxs-lookup"><span data-stu-id="87284-103">Error object</span></span>

<span data-ttu-id="87284-104">Объект **Error** возвращает сведения об одной ошибке слияния.</span><span class="sxs-lookup"><span data-stu-id="87284-104">The **Error** object returns the information of a single merge error.</span></span>

## <a name="members"></a><span data-ttu-id="87284-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="87284-105">Members</span></span>

<span data-ttu-id="87284-106">Объект **Error** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="87284-106">The **Error** object has these types of members:</span></span>

-   [<span data-ttu-id="87284-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="87284-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87284-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="87284-108">Properties</span></span>

<span data-ttu-id="87284-109">Объект **Error** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="87284-109">The **Error** object has these properties.</span></span>



| <span data-ttu-id="87284-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="87284-110">Property</span></span>                                                | <span data-ttu-id="87284-111">Описание</span><span class="sxs-lookup"><span data-stu-id="87284-111">Description</span></span>                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87284-112">**датабасекэйс**</span><span class="sxs-lookup"><span data-stu-id="87284-112">**DatabaseKeys**</span></span>](error-databasekeys.md)<br/>   | <span data-ttu-id="87284-113">Возвращает первичные ключи строки в таблице базы данных, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="87284-113">Returns the primary keys of the row in the database table that caused the error.</span></span><br/> |
| [<span data-ttu-id="87284-114">**датабасетабле**</span><span class="sxs-lookup"><span data-stu-id="87284-114">**DatabaseTable**</span></span>](error-databasetable.md)<br/> | <span data-ttu-id="87284-115">Возвращает имя таблицы в базе данных, вызвавшей ошибку.</span><span class="sxs-lookup"><span data-stu-id="87284-115">Returns the table name of the table in the database causing the error.</span></span><br/>           |
| [<span data-ttu-id="87284-116">**Язык**</span><span class="sxs-lookup"><span data-stu-id="87284-116">**Language**</span></span>](error-language.md)<br/>           | <span data-ttu-id="87284-117">Возврат языка ошибки.</span><span class="sxs-lookup"><span data-stu-id="87284-117">Return the language of the error.</span></span><br/>                                                |
| [<span data-ttu-id="87284-118">**модулекэйс**</span><span class="sxs-lookup"><span data-stu-id="87284-118">**ModuleKeys**</span></span>](error-modulekeys.md)<br/>       | <span data-ttu-id="87284-119">Возвращает первичные ключи строки в таблице Module, вызвавшие ошибку.</span><span class="sxs-lookup"><span data-stu-id="87284-119">Returns the primary keys of the row in the module table that caused the error.</span></span><br/>   |
| [<span data-ttu-id="87284-120">**модулетабле**</span><span class="sxs-lookup"><span data-stu-id="87284-120">**ModuleTable**</span></span>](error-moduletable.md)<br/>     | <span data-ttu-id="87284-121">Возвращает имя таблицы в модуле, вызвавшем ошибку.</span><span class="sxs-lookup"><span data-stu-id="87284-121">Returns the table name of the table in the module causing the error.</span></span><br/>             |
| [<span data-ttu-id="87284-122">**Путь**</span><span class="sxs-lookup"><span data-stu-id="87284-122">**Path**</span></span>](error-path.md)<br/>                   | <span data-ttu-id="87284-123">Возврат пути к файлу или каталогу, вызвавшему ошибку.</span><span class="sxs-lookup"><span data-stu-id="87284-123">Return the path to the file or directory causing the error.</span></span> <span data-ttu-id="87284-124">В настоящее время не используется.</span><span class="sxs-lookup"><span data-stu-id="87284-124">Currently unused.</span></span><br/>    |
| [<span data-ttu-id="87284-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="87284-125">**Type**</span></span>](error-type.md)<br/>                   | <span data-ttu-id="87284-126">Возврат типа ошибки.</span><span class="sxs-lookup"><span data-stu-id="87284-126">Return the type of error.</span></span><br/>                                                        |



 

## <a name="c"></a><span data-ttu-id="87284-127">C++</span><span class="sxs-lookup"><span data-stu-id="87284-127">C++</span></span>

<span data-ttu-id="87284-128">интерфейс **имсмеррор: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="87284-128">interface **IMsmError : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="87284-129">Идентификатор интерфейса</span><span class="sxs-lookup"><span data-stu-id="87284-129">Interface ID</span></span>



| <span data-ttu-id="87284-130">Константа</span><span class="sxs-lookup"><span data-stu-id="87284-130">Constant</span></span>           | <span data-ttu-id="87284-131">Значение</span><span class="sxs-lookup"><span data-stu-id="87284-131">Value</span></span>                                  |
|--------------------|----------------------------------------|
| <span data-ttu-id="87284-132">**IID \_ имсмеррор**</span><span class="sxs-lookup"><span data-stu-id="87284-132">**IID\_IMsmError**</span></span> | <span data-ttu-id="87284-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span><span class="sxs-lookup"><span data-stu-id="87284-133">{0ADDA828-2C26-11D2-AD65-00A0C9AF11A6}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="87284-134">Требования</span><span class="sxs-lookup"><span data-stu-id="87284-134">Requirements</span></span>



| <span data-ttu-id="87284-135">Требование</span><span class="sxs-lookup"><span data-stu-id="87284-135">Requirement</span></span> | <span data-ttu-id="87284-136">Значение</span><span class="sxs-lookup"><span data-stu-id="87284-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87284-137">Версия</span><span class="sxs-lookup"><span data-stu-id="87284-137">Version</span></span><br/> | <span data-ttu-id="87284-138">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="87284-138">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="87284-139">Header</span><span class="sxs-lookup"><span data-stu-id="87284-139">Header</span></span><br/>  | <dl> <span data-ttu-id="87284-140"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="87284-140"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="87284-141">DLL</span><span class="sxs-lookup"><span data-stu-id="87284-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="87284-142"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87284-142"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




