---
description: Удаляет подраздел и его значения из автономного куста реестра.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: Функция Орделетекэй (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: a122be2e738bb16730eee31772fc2c1c0671eddb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649008"
---
# <a name="ordeletekey-function"></a><span data-ttu-id="83137-103">Функция Орделетекэй</span><span class="sxs-lookup"><span data-stu-id="83137-103">ORDeleteKey function</span></span>

<span data-ttu-id="83137-104">Удаляет подраздел и его значения из автономного куста реестра.</span><span class="sxs-lookup"><span data-stu-id="83137-104">Deletes a subkey and its values from an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="83137-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83137-105">Syntax</span></span>


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a><span data-ttu-id="83137-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83137-107">*Обработчик* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83137-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83137-108">Маркер открытого раздела реестра в автономном кусте реестра.</span><span class="sxs-lookup"><span data-stu-id="83137-108">A handle to an open registry key in an offline registry hive.</span></span> <span data-ttu-id="83137-109">Этот маркер возвращается функцией [**оркреатекэй**](orcreatekey.md) или [**оропенкэй**](oropenkey.md) .</span><span class="sxs-lookup"><span data-stu-id="83137-109">This handle is returned by the [**ORCreateKey**](orcreatekey.md) or [**OROpenKey**](oropenkey.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="83137-110">*лпсубкэй* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="83137-110">*lpSubKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83137-111">Имя удаляемого ключа.</span><span class="sxs-lookup"><span data-stu-id="83137-111">The name of the key to be deleted.</span></span> <span data-ttu-id="83137-112">Он должен быть подразделом ключа, который *обрабатывает* определение, но не может иметь подразделы.</span><span class="sxs-lookup"><span data-stu-id="83137-112">It must be a subkey of the key that *Handle* identifies, but it cannot have subkeys.</span></span>

<span data-ttu-id="83137-113">Если подраздел не существует, функция возвращает ошибку \_ не \_ найдено.</span><span class="sxs-lookup"><span data-stu-id="83137-113">If the subkey does not exist, the function returns ERROR\_NOT\_FOUND.</span></span>

<span data-ttu-id="83137-114">Если этот параметр имеет **значение NULL**, функция удаляет ключ, заданный параметром *Handle* .</span><span class="sxs-lookup"><span data-stu-id="83137-114">If this parameter is **NULL**, the function deletes the key specified by the *Handle* parameter.</span></span> <span data-ttu-id="83137-115">Если ключ, заданный параметром *Handle* , является корневым ключом Hive, функция возвращает ошибку " \_ Недопустимый \_ параметр".</span><span class="sxs-lookup"><span data-stu-id="83137-115">If the key specified by the *Handle* parameter is the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="83137-116">Имена ключей не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="83137-116">Key names are not case sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83137-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83137-117">Return value</span></span>

<span data-ttu-id="83137-118">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="83137-118">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="83137-119">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="83137-119">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="83137-120">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="83137-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="83137-121">Ниже перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="83137-121">Possible error codes include the following:</span></span>

-   <span data-ttu-id="83137-122">Если указанный подраздел не существует, функция возвращает \_ файл ошибки \_ не \_ найден.</span><span class="sxs-lookup"><span data-stu-id="83137-122">If the specified subkey does not exist, the function returns ERROR\_FILE\_NOT\_FOUND.</span></span>
-   <span data-ttu-id="83137-123">Если указанный подраздел является корневым ключом куста реестра, функция возвращает ошибку " \_ Недопустимый \_ параметр".</span><span class="sxs-lookup"><span data-stu-id="83137-123">If the specified subkey is the root key of the registry hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>
-   <span data-ttu-id="83137-124">Если в указанном подразделе есть подразделы, функция возвращает \_ ключ ошибки \_ с \_ дочерними элементами.</span><span class="sxs-lookup"><span data-stu-id="83137-124">If the specified subkey has subkeys, the function returns ERROR\_KEY\_HAS\_CHILDREN.</span></span>

## <a name="remarks"></a><span data-ttu-id="83137-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83137-125">Remarks</span></span>

<span data-ttu-id="83137-126">Если указанный раздел реестра существует, он помечается как удаленный.</span><span class="sxs-lookup"><span data-stu-id="83137-126">If the specified registry key exists, it is marked as deleted.</span></span> <span data-ttu-id="83137-127">Удаленный ключ не удаляется до тех пор, пока последний его маркер не будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="83137-127">A deleted key is not removed until the last handle to it is closed.</span></span>

<span data-ttu-id="83137-128">Удаляемый ключ не должен иметь подразделов.</span><span class="sxs-lookup"><span data-stu-id="83137-128">The key to be deleted must not have subkeys.</span></span> <span data-ttu-id="83137-129">Чтобы удалить ключ и все его подразделы, используйте функцию [**оренумкэй**](orenumkey.md) , чтобы перечислить подразделы и удалить их по отдельности.</span><span class="sxs-lookup"><span data-stu-id="83137-129">To delete a key and all its subkeys, use the [**OREnumKey**](orenumkey.md) function to enumerate the subkeys and delete them individually.</span></span>

<span data-ttu-id="83137-130">Для удаленного ключа может быть вызвана только функция [**орклосекэй**](orclosekey.md) ; все остальные операции в автономном реестре завершаются ошибкой.</span><span class="sxs-lookup"><span data-stu-id="83137-130">Only the [**ORCloseKey**](orclosekey.md) function may be called on a deleted key; all other offline registry operations fail.</span></span> <span data-ttu-id="83137-131">Если удаленный ключ был явно создан путем вызова [**оркреатекэй**](orcreatekey.md), ресурсы, связанные с этим ключом, освобождаются при закрытии последнего маркера удаленного ключа.</span><span class="sxs-lookup"><span data-stu-id="83137-131">If the deleted key was explicitly created by calling [**ORCreateKey**](orcreatekey.md), resources associated with the key are released when the last handle to the deleted key is closed.</span></span>

## <a name="requirements"></a><span data-ttu-id="83137-132">Требования</span><span class="sxs-lookup"><span data-stu-id="83137-132">Requirements</span></span>



| <span data-ttu-id="83137-133">Требование</span><span class="sxs-lookup"><span data-stu-id="83137-133">Requirement</span></span> | <span data-ttu-id="83137-134">Значение</span><span class="sxs-lookup"><span data-stu-id="83137-134">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83137-135">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="83137-135">Redistributable</span></span><br/> | <span data-ttu-id="83137-136">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="83137-136">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="83137-137">Header</span><span class="sxs-lookup"><span data-stu-id="83137-137">Header</span></span><br/>          | <dl> <span data-ttu-id="83137-138"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="83137-138"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="83137-139">DLL</span><span class="sxs-lookup"><span data-stu-id="83137-139">DLL</span></span><br/>             | <dl> <span data-ttu-id="83137-140"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83137-140"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83137-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83137-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83137-142">**орклосекэй**</span><span class="sxs-lookup"><span data-stu-id="83137-142">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="83137-143">**оркреатекэй**</span><span class="sxs-lookup"><span data-stu-id="83137-143">**ORCreateKey**</span></span>](orcreatekey.md)
</dt> <dt>

[<span data-ttu-id="83137-144">**оренумкэй**</span><span class="sxs-lookup"><span data-stu-id="83137-144">**OREnumKey**</span></span>](orenumkey.md)
</dt> <dt>

[<span data-ttu-id="83137-145">**оропенкэй**</span><span class="sxs-lookup"><span data-stu-id="83137-145">**OROpenKey**</span></span>](oropenkey.md)
</dt> </dl>

 

 
