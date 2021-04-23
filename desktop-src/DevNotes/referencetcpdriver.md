---
description: Получает ссылку на объект драйвера TCP v4.
ms.assetid: 8f12fa58-1622-40d0-9a99-e7c8ede08b38
title: Функция Референцеткпдривер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriver
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: 4a9068739517cceedee72a675739b2d8b067b2ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649075"
---
# <a name="referencetcpdriver-function"></a><span data-ttu-id="92570-103">Функция Референцеткпдривер</span><span class="sxs-lookup"><span data-stu-id="92570-103">ReferenceTcpDriver function</span></span>

<span data-ttu-id="92570-104">Получает ссылку на объект драйвера TCP v4.</span><span class="sxs-lookup"><span data-stu-id="92570-104">Obtains a reference to a TCP v4 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="92570-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92570-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriver(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="92570-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92570-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92570-107">*ппдриверобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="92570-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92570-108">Указатель на структуру **\_ объектов драйвера** .</span><span class="sxs-lookup"><span data-stu-id="92570-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="92570-109">Дополнительные сведения см. в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="92570-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92570-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92570-110">Return value</span></span>

<span data-ttu-id="92570-111">Если функция завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="92570-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="92570-112">В случае сбоя он возвратит соответствующий код состояния.</span><span class="sxs-lookup"><span data-stu-id="92570-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="92570-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92570-113">Remarks</span></span>

<span data-ttu-id="92570-114">Эту функцию можно вызывать только из режима ядра.</span><span class="sxs-lookup"><span data-stu-id="92570-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="92570-115">Вызывающий объект должен уменьшить число ссылок, вызвав функцию **обдереференцеобжект** после завершения работы с объектом.</span><span class="sxs-lookup"><span data-stu-id="92570-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="92570-116">Эта функция реализована в Дрвреф. lib, которая доступна для загрузки.</span><span class="sxs-lookup"><span data-stu-id="92570-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="92570-117">См. раздел [Библиотека API справочника по сетевым драйверам Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="92570-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="92570-118">Требования</span><span class="sxs-lookup"><span data-stu-id="92570-118">Requirements</span></span>



| <span data-ttu-id="92570-119">Требование</span><span class="sxs-lookup"><span data-stu-id="92570-119">Requirement</span></span> | <span data-ttu-id="92570-120">Значение</span><span class="sxs-lookup"><span data-stu-id="92570-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92570-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92570-121">Library</span></span><br/> | <dl> <span data-ttu-id="92570-122"><dt>Дрвреф. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92570-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92570-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92570-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92570-124">**ReferenceTcpDriverV6**</span><span class="sxs-lookup"><span data-stu-id="92570-124">**ReferenceTcpDriverV6**</span></span>](referencetcpdriverv6.md)
</dt> </dl>

 

 




