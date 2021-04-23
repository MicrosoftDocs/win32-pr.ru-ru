---
description: Получает ссылку на объект драйвера TCP V6.
ms.assetid: 9f57ea0b-0ab4-4ef9-9bf1-1f41f72dfbe9
title: Функция ReferenceTcpDriverV6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReferenceTcpDriverV6
api_type:
- LibDef
api_location:
- Drvref.lib
ms.openlocfilehash: d0a3f56ea59eb753dc7a49d6f6b1d0c48be8abca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649045"
---
# <a name="referencetcpdriverv6-function"></a><span data-ttu-id="efc59-103">Функция ReferenceTcpDriverV6</span><span class="sxs-lookup"><span data-stu-id="efc59-103">ReferenceTcpDriverV6 function</span></span>

<span data-ttu-id="efc59-104">Получает ссылку на объект драйвера TCP V6.</span><span class="sxs-lookup"><span data-stu-id="efc59-104">Obtains a reference to a TCP v6 driver object.</span></span>

## <a name="syntax"></a><span data-ttu-id="efc59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efc59-105">Syntax</span></span>


```C++
NTSTATUS WINAPI ReferenceTcpDriverV6(
  _Out_ PDRIVER_OBJECT *ppDriverObject
);
```



## <a name="parameters"></a><span data-ttu-id="efc59-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="efc59-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efc59-107">*ппдриверобжект* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="efc59-107">*ppDriverObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efc59-108">Указатель на структуру **\_ объектов драйвера** .</span><span class="sxs-lookup"><span data-stu-id="efc59-108">A pointer to a **DRIVER\_OBJECT** structure.</span></span> <span data-ttu-id="efc59-109">Дополнительные сведения см. в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="efc59-109">For more information, see the documentation for the WDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efc59-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="efc59-110">Return value</span></span>

<span data-ttu-id="efc59-111">Если функция завершается успешно, возвращается **состояние \_ Success**.</span><span class="sxs-lookup"><span data-stu-id="efc59-111">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="efc59-112">В случае сбоя он возвратит соответствующий код состояния.</span><span class="sxs-lookup"><span data-stu-id="efc59-112">If it fails, it will return the appropriate status code.</span></span>

## <a name="remarks"></a><span data-ttu-id="efc59-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="efc59-113">Remarks</span></span>

<span data-ttu-id="efc59-114">Эту функцию можно вызывать только из режима ядра.</span><span class="sxs-lookup"><span data-stu-id="efc59-114">This function can be called only from kernel mode.</span></span> <span data-ttu-id="efc59-115">Вызывающий объект должен уменьшить число ссылок, вызвав функцию **обдереференцеобжект** после завершения работы с объектом.</span><span class="sxs-lookup"><span data-stu-id="efc59-115">The caller must decrement the reference count by calling the **ObDereferenceObject** function when it has finished with the object.</span></span>

<span data-ttu-id="efc59-116">Эта функция реализована в Дрвреф. lib, которая доступна для загрузки.</span><span class="sxs-lookup"><span data-stu-id="efc59-116">This function is implemented in Drvref.lib, which is available for download.</span></span> <span data-ttu-id="efc59-117">См. раздел [Библиотека API справочника по сетевым драйверам Windows](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span><span class="sxs-lookup"><span data-stu-id="efc59-117">See [Windows Network Driver Reference API Library](https://www.microsoft.com/downloads/details.aspx?FamilyID=85037e05-f8f8-46b4-a013-3aa6248396c0).</span></span>

## <a name="requirements"></a><span data-ttu-id="efc59-118">Требования</span><span class="sxs-lookup"><span data-stu-id="efc59-118">Requirements</span></span>



| <span data-ttu-id="efc59-119">Требование</span><span class="sxs-lookup"><span data-stu-id="efc59-119">Requirement</span></span> | <span data-ttu-id="efc59-120">Значение</span><span class="sxs-lookup"><span data-stu-id="efc59-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efc59-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="efc59-121">Library</span></span><br/> | <dl> <span data-ttu-id="efc59-122"><dt>Дрвреф. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efc59-122"><dt>Drvref.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc59-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efc59-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc59-124">**референцеткпдривер**</span><span class="sxs-lookup"><span data-stu-id="efc59-124">**ReferenceTcpDriver**</span></span>](referencetcpdriver.md)
</dt> </dl>

 

 




