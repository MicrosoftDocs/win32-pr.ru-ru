---
description: Метод Connect объекта Merge подключает модуль к дополнительному компоненту. Модуль уже должен быть объединен в базу данных или будет объединен в базу данных. Функция должна существовать до вызова этой функции.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Метод Merge. Connect (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665483"
---
# <a name="mergeconnect-method"></a><span data-ttu-id="b8d2a-105">Метод Merge. Connect</span><span class="sxs-lookup"><span data-stu-id="b8d2a-105">Merge.Connect method</span></span>

<span data-ttu-id="b8d2a-106">Метод **Connect** объекта [**Merge**](merge-object.md) подключает модуль к дополнительному компоненту.</span><span class="sxs-lookup"><span data-stu-id="b8d2a-106">The **Connect** method of the [**Merge**](merge-object.md) object connects a module to an additional feature.</span></span> <span data-ttu-id="b8d2a-107">Модуль уже должен быть объединен в базу данных или будет объединен в базу данных.</span><span class="sxs-lookup"><span data-stu-id="b8d2a-107">The module must have already been merged into the database or will be merged into the database.</span></span> <span data-ttu-id="b8d2a-108">Функция должна существовать до вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="b8d2a-108">The feature must exist before calling this function.</span></span>

<span data-ttu-id="b8d2a-109">Изменения, внесенные в базу данных, не сохраняются на диске, если метод [**клоседатабасе**](merge-closedatabase.md) не вызывается с параметром *бкоммит* , для которого задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="b8d2a-109">Changes made to the database are not saved to disk unless the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8d2a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8d2a-110">Syntax</span></span>


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a><span data-ttu-id="b8d2a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8d2a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8d2a-112">*Компонент*</span><span class="sxs-lookup"><span data-stu-id="b8d2a-112">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="b8d2a-113">Имя компонента, уже существующего в базе данных.</span><span class="sxs-lookup"><span data-stu-id="b8d2a-113">The name of a feature already existing in the database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8d2a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b8d2a-114">Return value</span></span>

<span data-ttu-id="b8d2a-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b8d2a-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8d2a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8d2a-116">Remarks</span></span>

<span data-ttu-id="b8d2a-117">Ошибки могут быть получены с помощью свойства [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="b8d2a-117">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="b8d2a-118">Ошибки и информационные сообщения отправляются в текущий файл журнала.</span><span class="sxs-lookup"><span data-stu-id="b8d2a-118">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="b8d2a-119">C++</span><span class="sxs-lookup"><span data-stu-id="b8d2a-119">C++</span></span>

<span data-ttu-id="b8d2a-120">См. раздел Функция [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) .</span><span class="sxs-lookup"><span data-stu-id="b8d2a-120">See [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8d2a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="b8d2a-121">Requirements</span></span>



| <span data-ttu-id="b8d2a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="b8d2a-122">Requirement</span></span> | <span data-ttu-id="b8d2a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="b8d2a-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8d2a-124">Версия</span><span class="sxs-lookup"><span data-stu-id="b8d2a-124">Version</span></span><br/> | <span data-ttu-id="b8d2a-125">Mergemod.dll 1,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b8d2a-125">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="b8d2a-126">Header</span><span class="sxs-lookup"><span data-stu-id="b8d2a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b8d2a-127"><dt>Мержемод. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8d2a-127"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8d2a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b8d2a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8d2a-129"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8d2a-129"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
