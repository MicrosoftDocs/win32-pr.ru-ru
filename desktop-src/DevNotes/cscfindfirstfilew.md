---
description: Выполняет поиск файла в кэше автономные файлы, который соответствует указанным критериям.
ms.assetid: 09de6c55-fc37-4c0a-b5a0-ea73f06793d5
title: Функция Кскфиндфирстфилев
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindFirstFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: f8cad9caf78b44f40a4126307db6deb0f71dfd1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648924"
---
# <a name="cscfindfirstfilew-function"></a><span data-ttu-id="2ecc3-103">Функция Кскфиндфирстфилев</span><span class="sxs-lookup"><span data-stu-id="2ecc3-103">CSCFindFirstFileW function</span></span>

<span data-ttu-id="2ecc3-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="2ecc3-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="2ecc3-105">Выполняет поиск файла в кэше автономные файлы, который соответствует указанным критериям.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-105">Searches for a file in the Offline Files cache that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ecc3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ecc3-106">Syntax</span></span>


```C++
HANDLE WINAPI CSCFindFirstFileW(
  _In_  LPCWSTR          lpszFileName,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _Out_ FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="2ecc3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ecc3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ecc3-108">*лпсзфиленаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ecc3-108">*lpszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecc3-109">Указатель на строку, завершающуюся нулем, которая указывает допустимый UNC-каталог или путь.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-109">A pointer to a null-terminated string that specifies a valid UNC directory or path.</span></span>

</dd> <dt>

<span data-ttu-id="2ecc3-110">*lpFind32* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ecc3-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecc3-111">Указатель на структуру [**данных Win32 \_ Find \_**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) , которая получает сведения о файле или подкаталоге.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="2ecc3-112">*лпдвстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ecc3-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecc3-113">Код NTSTATUS, указывающий состояние вызова.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="2ecc3-114">*лпдвпинкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ecc3-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecc3-115">Этот параметр имеет ненулевое значение, если файл был сделан доступным в автономном режиме или 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="2ecc3-116">*лпдвхинтфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ecc3-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecc3-117">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="2ecc3-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2ecc3-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="2ecc3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="2ecc3-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="2ecc3-120"><dt>**Флаг \_ \_Код CSC \_ Указание \_ пользователя**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="2ecc3-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="2ecc3-121">Пользователь сделал файл доступным в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="2ecc3-122"><dt>**Флаг \_ \_ \_ ПИН-код подсказки CSC \_ наследует \_ пользователя**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="2ecc3-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="2ecc3-123">Пользователь сделал родительский доступ к автономной версии и отметил родительский элемент таким образом, чтобы его дочерние элементы были доступны в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="2ecc3-124"><dt>**Флаг \_ \_ \_ ПИН-код ПОДсказок CSC \_ наследует \_ системные**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="2ecc3-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="2ecc3-125">Администратор или групповая политика выполнила доступ к родительскому объекту в автономном режиме и отметил родительский элемент таким образом, что его дочерние элементы доступны в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="2ecc3-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="2ecc3-126"><dt>**Флаг \_ Подсказка CSC для \_ \_ \_ системы закрепления**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="2ecc3-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="2ecc3-127">Администратор или групповая политика выполнила автономный доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="2ecc3-128">*лпоргфилетиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2ecc3-128">*lpOrgFileTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ecc3-129">Указатель на структуру [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) для получения сведений о дате и времени для файла или подкаталога.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ecc3-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ecc3-130">Return value</span></span>

<span data-ttu-id="2ecc3-131">Если функция выполнена, возвращаемое значение является маркером поиска, используемым при последующем вызове метода [**кскфинднекстфилев**](cscfindnextfilew.md) или [**кскфиндклосе**](cscfindclose.md).</span><span class="sxs-lookup"><span data-stu-id="2ecc3-131">If the function succeeds, the return value is a search handle used in a subsequent call to [**CSCFindNextFileW**](cscfindnextfilew.md) or [**CSCFindClose**](cscfindclose.md).</span></span>

<span data-ttu-id="2ecc3-132">Если функция выполняется неудачно, возвращается значение **INVALID\_HANDLE\_VALUE**.</span><span class="sxs-lookup"><span data-stu-id="2ecc3-132">If the function fails, the return value is **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ecc3-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ecc3-133">Remarks</span></span>

<span data-ttu-id="2ecc3-134">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2ecc3-134">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ecc3-135">Требования</span><span class="sxs-lookup"><span data-stu-id="2ecc3-135">Requirements</span></span>



| <span data-ttu-id="2ecc3-136">Требование</span><span class="sxs-lookup"><span data-stu-id="2ecc3-136">Requirement</span></span> | <span data-ttu-id="2ecc3-137">Значение</span><span class="sxs-lookup"><span data-stu-id="2ecc3-137">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ecc3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2ecc3-138">DLL</span></span><br/> | <dl> <span data-ttu-id="2ecc3-139"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ecc3-139"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
