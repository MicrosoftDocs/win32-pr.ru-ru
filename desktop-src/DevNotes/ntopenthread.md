---
description: Открывает обработчик для объекта потока с указанным доступом.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: Функция Нтопенсреад
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648751"
---
# <a name="ntopenthread-function"></a><span data-ttu-id="7e339-103">Функция Нтопенсреад</span><span class="sxs-lookup"><span data-stu-id="7e339-103">NtOpenThread function</span></span>

<span data-ttu-id="7e339-104">\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.</span><span class="sxs-lookup"><span data-stu-id="7e339-104">\[This function may be changed or removed from Windows without further notice.</span></span> <span data-ttu-id="7e339-105">Вместо этого используйте функцию [**опенсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]</span><span class="sxs-lookup"><span data-stu-id="7e339-105">Use the [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function instead.\]</span></span>

<span data-ttu-id="7e339-106">Открывает обработчик для объекта потока с указанным доступом.</span><span class="sxs-lookup"><span data-stu-id="7e339-106">Opens a handle to a thread object with the access specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e339-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7e339-107">Syntax</span></span>


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a><span data-ttu-id="7e339-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e339-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e339-109">*Среадхандле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7e339-109">*ThreadHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e339-110">Указатель на переменную, которая получает обработчик объекта потока.</span><span class="sxs-lookup"><span data-stu-id="7e339-110">A pointer to a variable that receives the thread object handle.</span></span>

</dd> <dt>

<span data-ttu-id="7e339-111">*Десиредакцесс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e339-111">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e339-112">Тип [**данных \_ маски доступа**](../secauthz/access-mask-format.md) , предоставляющий требуемые типы доступа для объекта потока.</span><span class="sxs-lookup"><span data-stu-id="7e339-112">An [**ACCESS\_MASK**](../secauthz/access-mask-format.md) data type that provides the desired types of access for the thread object.</span></span>

</dd> <dt>

<span data-ttu-id="7e339-113">*Обжектаттрибутес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e339-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e339-114">Указатель на структуру [ \_ атрибутов объекта](https://msdn.microsoft.com/library/aa491657.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7e339-114">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure.</span></span> <span data-ttu-id="7e339-115">Элемент **objectname** этой структуры должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="7e339-115">The **ObjectName** member of this structure must be NULL.</span></span>

<span data-ttu-id="7e339-116">**Windows Server 2003 и Windows XP:** Элемент **objectname** этой структуры может указывать на имя объекта.</span><span class="sxs-lookup"><span data-stu-id="7e339-116">**Windows Server 2003 and Windows XP:** The **ObjectName** member of this structure can point to an object name.</span></span> <span data-ttu-id="7e339-117">Если **objectname** не равен null, параметр *ClientID* должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="7e339-117">If **ObjectName** is not NULL, the *ClientId* parameter must be NULL.</span></span>

</dd> <dt>

<span data-ttu-id="7e339-118">*ClientID* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7e339-118">*ClientId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e339-119">Указатель на структуру **\_ идентификатора клиента** , определяющую поток, чей поток должен быть открыт.</span><span class="sxs-lookup"><span data-stu-id="7e339-119">A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span>

<span data-ttu-id="7e339-120">**Windows Server 2003 и Windows XP:** Указатель на структуру **\_ идентификатора клиента** , определяющую поток, чей поток должен быть открыт.</span><span class="sxs-lookup"><span data-stu-id="7e339-120">**Windows Server 2003 and Windows XP:** A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span> <span data-ttu-id="7e339-121">Этот параметр может принимать значение NULL.</span><span class="sxs-lookup"><span data-stu-id="7e339-121">This parameter can be NULL.</span></span> <span data-ttu-id="7e339-122">Если этот параметр не равен NULL, то элемент **objectname** структуры, на который указывает параметр *обжектаттрибутес* , должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="7e339-122">If this parameter is not NULL, the **ObjectName** member of the structure pointed to by the *ObjectAttributes* parameter must be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e339-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e339-123">Return value</span></span>

<span data-ttu-id="7e339-124">Возвращает код **NTSTATUS** или ошибки.</span><span class="sxs-lookup"><span data-stu-id="7e339-124">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="7e339-125">Формы и значения кодов ошибок **NTSTATUS** перечислены в файле заголовка NTSTATUS. h, доступном в WDK, и описаны в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="7e339-125">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e339-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7e339-126">Remarks</span></span>

<span data-ttu-id="7e339-127">Эта функция не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="7e339-127">This function has no associated header file.</span></span> <span data-ttu-id="7e339-128">Связанная библиотека импорта, NTDLL. lib, доступна в WDK.</span><span class="sxs-lookup"><span data-stu-id="7e339-128">The associated import library, Ntdll.lib is available in the WDK.</span></span> <span data-ttu-id="7e339-129">Можно также использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="7e339-129">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e339-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7e339-130">Requirements</span></span>



| <span data-ttu-id="7e339-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7e339-131">Requirement</span></span> | <span data-ttu-id="7e339-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7e339-132">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7e339-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7e339-133">DLL</span></span><br/> | <dl> <span data-ttu-id="7e339-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e339-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
