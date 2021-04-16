---
description: Возобновляет операцию поиска файлов.
ms.assetid: 5b1a8f67-7fce-4ba5-918d-826bdaca1947
title: Функция Кскфинднекстфилев
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCFindNextFileW
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 50b387a1ff99a95fcbe0fae8fe8ad93d14c335b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657425"
---
# <a name="cscfindnextfilew-function"></a><span data-ttu-id="932f6-103">Функция Кскфинднекстфилев</span><span class="sxs-lookup"><span data-stu-id="932f6-103">CSCFindNextFileW function</span></span>

<span data-ttu-id="932f6-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="932f6-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="932f6-105">Возобновляет операцию поиска файлов.</span><span class="sxs-lookup"><span data-stu-id="932f6-105">Continues a file search operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="932f6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="932f6-106">Syntax</span></span>


```C++
BOOL WINAPI CSCFindNextFileW(
  _In_  HANDLE           hFind,
  _Out_ WIN32_FIND_DATAW *lpFind32,
  _Out_ LPDWORD          lpdwStatus,
  _Out_ LPDWORD          lpdwPinCount,
  _Out_ LPDWORD          lpdwHintFlags,
  _In_  FILETIME         *lpOrgFileTime
);
```



## <a name="parameters"></a><span data-ttu-id="932f6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="932f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="932f6-108">*хфинд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="932f6-108">*hFind* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="932f6-109">Маркер поиска, возвращаемый функцией [**кскфиндфирстфилев**](cscfindfirstfilew.md) .</span><span class="sxs-lookup"><span data-stu-id="932f6-109">A search handle returned by the [**CSCFindFirstFileW**](cscfindfirstfilew.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="932f6-110">*lpFind32* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="932f6-110">*lpFind32* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="932f6-111">Указатель на структуру [**данных Win32 \_ Find \_**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) , которая получает сведения о файле или подкаталоге.</span><span class="sxs-lookup"><span data-stu-id="932f6-111">A pointer to the [**WIN32\_FIND\_DATA**](/windows/win32/api/minwinbase/ns-minwinbase-win32_find_dataa) structure that receives information about the file or subdirectory.</span></span>

</dd> <dt>

<span data-ttu-id="932f6-112">*лпдвстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="932f6-112">*lpdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="932f6-113">Код NTSTATUS, указывающий состояние вызова.</span><span class="sxs-lookup"><span data-stu-id="932f6-113">An NTSTATUS code that indicates the status of the call.</span></span>

</dd> <dt>

<span data-ttu-id="932f6-114">*лпдвпинкаунт* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="932f6-114">*lpdwPinCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="932f6-115">Этот параметр имеет ненулевое значение, если файл был сделан доступным в автономном режиме или 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="932f6-115">This parameter is nonzero if the file has been made available offline or 0 otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="932f6-116">*лпдвхинтфлагс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="932f6-116">*lpdwHintFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="932f6-117">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="932f6-117">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="932f6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="932f6-118">Value</span></span>                                                                                                                                                                                                                                                                                | <span data-ttu-id="932f6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="932f6-119">Meaning</span></span>                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAG_CSC_HINT_PIN_USER"></span><span id="flag_csc_hint_pin_user"></span><dl> <span data-ttu-id="932f6-120"><dt>**Флаг \_ \_Код CSC \_ Указание \_ пользователя**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="932f6-120"><dt>**FLAG\_CSC\_HINT\_PIN\_USER**</dt> <dt>0x01</dt></span></span> </dl>                                | <span data-ttu-id="932f6-121">Пользователь сделал файл доступным в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="932f6-121">A user has made the file available offline.</span></span><br/>                                                                                                |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_USER"></span><span id="flag_csc_hint_pin_inherit_user"></span><dl> <span data-ttu-id="932f6-122"><dt>**Флаг \_ \_ \_ ПИН-код подсказки CSC \_ наследует \_ пользователя**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="932f6-122"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_USER**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="932f6-123">Пользователь сделал родительский доступ к автономной версии и отметил родительский элемент таким образом, чтобы его дочерние элементы были доступны в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="932f6-123">A user has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/>                           |
| <span id="FLAG_CSC_HINT_PIN_INHERIT_SYSTEM"></span><span id="flag_csc_hint_pin_inherit_system"></span><dl> <span data-ttu-id="932f6-124"><dt>**Флаг \_ \_ \_ ПИН-код ПОДсказок CSC \_ наследует \_ системные**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="932f6-124"><dt>**FLAG\_CSC\_HINT\_PIN\_INHERIT\_SYSTEM**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="932f6-125">Администратор или групповая политика выполнила доступ к родительскому объекту в автономном режиме и отметил родительский элемент таким образом, что его дочерние элементы доступны в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="932f6-125">An administrator or group policy has made the parent available offline and marked the parent such that its children are available offline.</span></span><br/> |
| <span id="FLAG_CSC_HINT_PIN_SYSTEM"></span><span id="flag_csc_hint_pin_system"></span><dl> <span data-ttu-id="932f6-126"><dt>**Флаг \_ Подсказка CSC для \_ \_ \_ системы закрепления**</dt> <dt>0x10</dt></span><span class="sxs-lookup"><span data-stu-id="932f6-126"><dt>**FLAG\_CSC\_HINT\_PIN\_SYSTEM**</dt> <dt>0x10</dt></span></span> </dl>                          | <span data-ttu-id="932f6-127">Администратор или групповая политика выполнила автономный доступ к файлу.</span><span class="sxs-lookup"><span data-stu-id="932f6-127">An administrator or group policy has made the file available offline.</span></span><br/>                                                                      |



 

</dd> <dt>

<span data-ttu-id="932f6-128">*лпоргфилетиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="932f6-128">*lpOrgFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="932f6-129">Указатель на структуру [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) для получения сведений о дате и времени для файла или подкаталога.</span><span class="sxs-lookup"><span data-stu-id="932f6-129">A pointer to a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure to receive the date and time information for the file or subdirectory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="932f6-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="932f6-130">Return value</span></span>

<span data-ttu-id="932f6-131">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="932f6-131">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="932f6-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="932f6-132">Remarks</span></span>

<span data-ttu-id="932f6-133">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="932f6-133">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="932f6-134">Требования</span><span class="sxs-lookup"><span data-stu-id="932f6-134">Requirements</span></span>



| <span data-ttu-id="932f6-135">Требование</span><span class="sxs-lookup"><span data-stu-id="932f6-135">Requirement</span></span> | <span data-ttu-id="932f6-136">Значение</span><span class="sxs-lookup"><span data-stu-id="932f6-136">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="932f6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="932f6-137">DLL</span></span><br/> | <dl> <span data-ttu-id="932f6-138"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="932f6-138"><dt>Cscmig.dll</dt></span></span> </dl> |



 

 
