---
description: Загружает указанный файл куста реестра в память и проверяет куст.
ms.assetid: 5d8498b0-e1bb-4c3d-bf3d-7bfc3002eb1a
title: Функция Оропенхиве (Оффрег. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ba6531e7a2ab2b0b148065d9f4666812e75f2968
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669016"
---
# <a name="oropenhive-function"></a><span data-ttu-id="919ca-103">Функция Оропенхиве</span><span class="sxs-lookup"><span data-stu-id="919ca-103">OROpenHive function</span></span>

<span data-ttu-id="919ca-104">Загружает указанный файл куста реестра в память и проверяет куст.</span><span class="sxs-lookup"><span data-stu-id="919ca-104">Loads the specified registry hive file into memory and validates the hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="919ca-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="919ca-105">Syntax</span></span>


```C++
DWORD OROpenHive(
  _In_  PCWSTR  lpHivePath,
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a><span data-ttu-id="919ca-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="919ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="919ca-107">*лфивепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="919ca-107">*lpHivePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="919ca-108">Указатель на строку в Юникоде, указывающую имя файла куста реестра, который будет загружен в память.</span><span class="sxs-lookup"><span data-stu-id="919ca-108">A pointer to a Unicode string that specifies the name of the registry hive file to be loaded into memory.</span></span> <span data-ttu-id="919ca-109">Это может быть файл Hive, сохраненный с помощью функции [**орсавехиве**](orsavehive.md) или созданный с помощью функции [регсавекэй](/windows/win32/api/winreg/nf-winreg-regsavekeya) или [регсавекэйекс](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) .</span><span class="sxs-lookup"><span data-stu-id="919ca-109">This can be a hive file that was saved with the [**ORSaveHive**](orsavehive.md) function or created with the [RegSaveKey](/windows/win32/api/winreg/nf-winreg-regsavekeya) or [RegSaveKeyEx](/windows/win32/api/winreg/nf-winreg-regsavekeyexa) function.</span></span> <span data-ttu-id="919ca-110">Размер файла должен быть менее 4 ГБ, и вызывающая сторона должна иметь \_ \_ доступ к файлу для чтения данных.</span><span class="sxs-lookup"><span data-stu-id="919ca-110">The file must be less than 4 GB in size, and the caller must have FILE\_READ\_DATA access to the file.</span></span> <span data-ttu-id="919ca-111">Дополнительные сведения см. в разделе [безопасность и права доступа к файлам](../fileio/file-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="919ca-111">For more information, see [File Security and Access Rights](../fileio/file-security-and-access-rights.md).</span></span>

</dd> <dt>

<span data-ttu-id="919ca-112">*фкресулт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="919ca-112">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="919ca-113">Указатель на переменную, которая получает маркер корневого ключа загруженного куста реестра.</span><span class="sxs-lookup"><span data-stu-id="919ca-113">A pointer to a variable that receives a handle to the root key of the loaded offline registry hive.</span></span> <span data-ttu-id="919ca-114">Если не удается открыть файл куста реестра или выполнить проверку не удается, функция присваивает этому параметру **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="919ca-114">If the registry hive file cannot be opened or validation fails, the function sets this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="919ca-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="919ca-115">Return value</span></span>

<span data-ttu-id="919ca-116">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="919ca-116">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="919ca-117">Если функция завершается ошибкой, возвращаемое значение является ненулевым кодом ошибки, определенным в файле Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="919ca-117">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="919ca-118">[](/windows/win32/api/winbase/nf-winbase-formatmessage) \_ \_ \_ Для получения обобщенного описания ошибки можно использовать функцию FormatMessage с флагом формата Message от System.</span><span class="sxs-lookup"><span data-stu-id="919ca-118">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span> <span data-ttu-id="919ca-119">Ниже перечислены возможные коды ошибок.</span><span class="sxs-lookup"><span data-stu-id="919ca-119">Possible error codes include the following:</span></span>

-   <span data-ttu-id="919ca-120">Если файл пуст или имеет размер более 4 ГБ, функция возвращает ошибку \_ баддб.</span><span class="sxs-lookup"><span data-stu-id="919ca-120">If the file is empty or larger than 4 GB in size, the function returns ERROR\_BADDB.</span></span>
-   <span data-ttu-id="919ca-121">Если вызывающий объект не имеет необходимых прав доступа для открытия файла, функция возвращает сообщение об ошибке \_ отказа в доступе \_ .</span><span class="sxs-lookup"><span data-stu-id="919ca-121">If the caller does not have the necessary access rights to open the file, the function returns ERROR\_ACCESS\_DENIED.</span></span>
-   <span data-ttu-id="919ca-122">Если куст реестра не проходит проверку, функция возвращает ошибку \_ без \_ файла реестра \_ .</span><span class="sxs-lookup"><span data-stu-id="919ca-122">If the registry hive fails validation, the function returns ERROR\_NOT\_REGISTRY\_FILE.</span></span>

## <a name="remarks"></a><span data-ttu-id="919ca-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="919ca-123">Remarks</span></span>

<span data-ttu-id="919ca-124">Функция **оропенхиве** является единственной автономной функцией реестра, которая проверяет куст реестра.</span><span class="sxs-lookup"><span data-stu-id="919ca-124">The **OROpenHive** function is the only offline registry function that validates a registry hive.</span></span> <span data-ttu-id="919ca-125">Если проверка не удалась, попытка восстановления куста не выполняется.</span><span class="sxs-lookup"><span data-stu-id="919ca-125">If the validation fails, no attempt is made to repair the hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="919ca-126">Требования</span><span class="sxs-lookup"><span data-stu-id="919ca-126">Requirements</span></span>



| <span data-ttu-id="919ca-127">Требование</span><span class="sxs-lookup"><span data-stu-id="919ca-127">Requirement</span></span> | <span data-ttu-id="919ca-128">Значение</span><span class="sxs-lookup"><span data-stu-id="919ca-128">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="919ca-129">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="919ca-129">Redistributable</span></span><br/> | <span data-ttu-id="919ca-130">Автономная библиотека реестра Windows версии 1,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="919ca-130">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="919ca-131">Header</span><span class="sxs-lookup"><span data-stu-id="919ca-131">Header</span></span><br/>          | <dl> <span data-ttu-id="919ca-132"><dt>Оффрег. h</dt></span><span class="sxs-lookup"><span data-stu-id="919ca-132"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="919ca-133">DLL</span><span class="sxs-lookup"><span data-stu-id="919ca-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="919ca-134"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="919ca-134"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="919ca-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="919ca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="919ca-136">**орклосехиве**</span><span class="sxs-lookup"><span data-stu-id="919ca-136">**ORCloseHive**</span></span>](orclosehive.md)
</dt> <dt>

[<span data-ttu-id="919ca-137">**оркреатехиве**</span><span class="sxs-lookup"><span data-stu-id="919ca-137">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="919ca-138">**орсавехиве**</span><span class="sxs-lookup"><span data-stu-id="919ca-138">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="919ca-139">регсавекэй</span><span class="sxs-lookup"><span data-stu-id="919ca-139">RegSaveKey</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeya)
</dt> <dt>

[<span data-ttu-id="919ca-140">регсавекэйекс</span><span class="sxs-lookup"><span data-stu-id="919ca-140">RegSaveKeyEx</span></span>](/windows/win32/api/winreg/nf-winreg-regsavekeyexa)
</dt> </dl>

 

 
