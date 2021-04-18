---
description: Указатель на функцию, которая вызывается из точки входа библиотеки DLL.
ms.assetid: 30196657-38ab-42ca-b673-b0894999e566
title: Указатель функции Лпфнинитраутине (Комбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNInitRoutine
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 375660399180196e2434030ea7551733affc4062
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675376"
---
# <a name="lpfninitroutine-function-pointer"></a><span data-ttu-id="bffd4-103">Указатель функции Лпфнинитраутине</span><span class="sxs-lookup"><span data-stu-id="bffd4-103">LPFNInitRoutine function pointer</span></span>

<span data-ttu-id="bffd4-104">Указатель на функцию, которая вызывается из точки входа библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="bffd4-104">Pointer to a function that gets called from the DLL entry point.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffd4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bffd4-105">Syntax</span></span>


```C++
typedef void ( CALLBACK *LPFNInitRoutine)(
         BOOL  bLoading,
   const CLSID *rclsid
);
```



## <a name="parameters"></a><span data-ttu-id="bffd4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bffd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bffd4-107">*блоадинг*</span><span class="sxs-lookup"><span data-stu-id="bffd4-107">*bLoading*</span></span> 
</dt> <dd>

<span data-ttu-id="bffd4-108">**Значение true** , если библиотека DLL загружена, и **false** при выгрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="bffd4-108">**TRUE** when the DLL is loaded, **FALSE** when the DLL is unloaded.</span></span>

</dd> <dt>

<span data-ttu-id="bffd4-109">*рклсид*</span><span class="sxs-lookup"><span data-stu-id="bffd4-109">*rclsid*</span></span> 
</dt> <dd>

<span data-ttu-id="bffd4-110">Указатель на CLISD ИНИЦИАЛИЗИРОВАННОГО объекта, указанный в переменной члена [**\_ CLSID кфакторитемплате:: m**](cfactorytemplate-m-clsid.md) .</span><span class="sxs-lookup"><span data-stu-id="bffd4-110">Pointer to the object's CLISD, specified in the [**CFactoryTemplate::m\_ClsID**](cfactorytemplate-m-clsid.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bffd4-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bffd4-111">Return value</span></span>

<span data-ttu-id="bffd4-112">Этот указатель функции не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bffd4-112">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bffd4-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bffd4-113">Requirements</span></span>



| <span data-ttu-id="bffd4-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bffd4-114">Requirement</span></span> | <span data-ttu-id="bffd4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bffd4-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bffd4-116">Header</span><span class="sxs-lookup"><span data-stu-id="bffd4-116">Header</span></span><br/> | <dl> <span data-ttu-id="bffd4-117"><dt>Комбасе. h (включение Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bffd4-117"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bffd4-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bffd4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffd4-119">**Класс Кфакторитемплате**</span><span class="sxs-lookup"><span data-stu-id="bffd4-119">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




