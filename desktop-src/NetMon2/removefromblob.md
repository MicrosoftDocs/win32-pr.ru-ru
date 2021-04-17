---
description: Функция Ремовефромблоб удаляет любой уровень записи BLOB-объекта (владельца, категории или тега).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Функция Ремовефромблоб (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673253"
---
# <a name="removefromblob-function"></a><span data-ttu-id="25ccc-103">Функция Ремовефромблоб</span><span class="sxs-lookup"><span data-stu-id="25ccc-103">RemoveFromBlob function</span></span>

<span data-ttu-id="25ccc-104">Функция **ремовефромблоб** удаляет любой уровень записи BLOB-объекта (**владельца**, **категории** или **тега**).</span><span class="sxs-lookup"><span data-stu-id="25ccc-104">The **RemoveFromBlob** function deletes any level of BLOB entry (**Owner**, **Category**, or **Tag**).</span></span>

## <a name="syntax"></a><span data-ttu-id="25ccc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25ccc-105">Syntax</span></span>


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a><span data-ttu-id="25ccc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="25ccc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25ccc-107">*хблоб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25ccc-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccc-108">Обработчик для большого двоичного объекта, из которого удаляется запись.</span><span class="sxs-lookup"><span data-stu-id="25ccc-108">Handle to the BLOB from which an entry is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="25ccc-109">*повнернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25ccc-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccc-110">Указатель на имя **владельца** .</span><span class="sxs-lookup"><span data-stu-id="25ccc-110">Pointer to the **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="25ccc-111">*пкатегоринаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25ccc-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccc-112">Указатель на имя **категории** .</span><span class="sxs-lookup"><span data-stu-id="25ccc-112">Pointer to the **Category** name.</span></span> <span data-ttu-id="25ccc-113">Значение параметра **null** указывает, что вызывающий объект пытается удалить сведения о заданных **владельцах** и все его дочерние записи.</span><span class="sxs-lookup"><span data-stu-id="25ccc-113">A **NULL** parameter value indicates the caller is attempting to delete the given **Owner** information and all of its child entries.</span></span> <span data-ttu-id="25ccc-114">Обратите внимание, что если значение параметра *пкатегоринаме* равно **null**, параметр *Птагнаме* также должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="25ccc-114">Note that if the *pCategoryName* parameter value is **NULL**, the *pTagName* parameter must also be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="25ccc-115">*птагнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25ccc-115">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25ccc-116">Указатель на имя **тега** .</span><span class="sxs-lookup"><span data-stu-id="25ccc-116">Pointer to the **Tag** name.</span></span> <span data-ttu-id="25ccc-117">Значение _птагнаме_ , равное NULL, указывает вызывающему объекту, что пытается удалить данную **категорию** и все ее дочерние записи.</span><span class="sxs-lookup"><span data-stu-id="25ccc-117">A **NULL**_pTagName_ value indicates the caller is attempting to delete the given **Category** and all of its child entries.</span></span> <span data-ttu-id="25ccc-118">Если значение параметра не равно **null**, вызывающий объект запрашивает удаление только указанных записей **тега** .</span><span class="sxs-lookup"><span data-stu-id="25ccc-118">If the parameter value is not **NULL**, the caller is asking that only that the specified **Tag** entries be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25ccc-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25ccc-119">Return value</span></span>

<span data-ttu-id="25ccc-120">Если функция выполнена успешно, возвращается значение НМЕРР \_ Success.</span><span class="sxs-lookup"><span data-stu-id="25ccc-120">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="25ccc-121">Если функция завершается неудачно, возвращается значение НМЕРР, указывающее на ошибку.</span><span class="sxs-lookup"><span data-stu-id="25ccc-121">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="25ccc-122">Требования</span><span class="sxs-lookup"><span data-stu-id="25ccc-122">Requirements</span></span>



| <span data-ttu-id="25ccc-123">Требование</span><span class="sxs-lookup"><span data-stu-id="25ccc-123">Requirement</span></span> | <span data-ttu-id="25ccc-124">Значение</span><span class="sxs-lookup"><span data-stu-id="25ccc-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25ccc-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25ccc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="25ccc-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25ccc-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="25ccc-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25ccc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="25ccc-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="25ccc-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25ccc-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="25ccc-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="25ccc-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="25ccc-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="25ccc-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="25ccc-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="25ccc-132"><dt>Нпптулс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25ccc-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="25ccc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="25ccc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25ccc-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25ccc-134"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




