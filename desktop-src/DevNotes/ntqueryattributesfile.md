---
description: Извлекает основные атрибуты для указанного файлового объекта.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: Функция Нткуеряттрибутесфиле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665366"
---
# <a name="ntqueryattributesfile-function"></a><span data-ttu-id="c4796-103">Функция Нткуеряттрибутесфиле</span><span class="sxs-lookup"><span data-stu-id="c4796-103">NtQueryAttributesFile function</span></span>

<span data-ttu-id="c4796-104">\[Эта функция может быть изменена или удалена из Windows без предварительного уведомления.\]</span><span class="sxs-lookup"><span data-stu-id="c4796-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="c4796-105">Извлекает основные атрибуты для указанного файлового объекта.</span><span class="sxs-lookup"><span data-stu-id="c4796-105">Retrieves basic attributes for the specified file object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4796-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4796-106">Syntax</span></span>


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a><span data-ttu-id="c4796-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c4796-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4796-108">*Обжектаттрибутес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c4796-108">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4796-109">Указатель на структуру [ \_ атрибутов объекта](https://msdn.microsoft.com/library/aa491657.aspx) , которая предоставляет атрибуты, используемые для файлового объекта.</span><span class="sxs-lookup"><span data-stu-id="c4796-109">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure that supplies the attributes to be used for the file object.</span></span>

</dd> <dt>

<span data-ttu-id="c4796-110">*Филеинформатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c4796-110">*FileInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4796-111">Указатель на [ \_ \_ информационную структуру файла Basic](https://msdn.microsoft.com/library/aa491634.aspx) для получения возвращаемых сведений об атрибутах файла.</span><span class="sxs-lookup"><span data-stu-id="c4796-111">A pointer to a [FILE\_BASIC\_INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) structure to receive the returned file attribute information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4796-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c4796-112">Return value</span></span>

<span data-ttu-id="c4796-113">Возвращает код NTSTATUS или ошибки.</span><span class="sxs-lookup"><span data-stu-id="c4796-113">Returns an NTSTATUS or error code.</span></span>

<span data-ttu-id="c4796-114">Формы и значения кодов ошибок NTSTATUS перечислены в файле заголовка NTSTATUS. h, доступном в WDK, и описаны в документации по WDK.</span><span class="sxs-lookup"><span data-stu-id="c4796-114">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4796-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c4796-115">Remarks</span></span>

<span data-ttu-id="c4796-116">Эта функция не имеет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="c4796-116">This function has no associated header file.</span></span> <span data-ttu-id="c4796-117">Связанная библиотека импорта, NTDLL. lib, доступна в WDK.</span><span class="sxs-lookup"><span data-stu-id="c4796-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="c4796-118">Можно также использовать функции [**LoadLibrary**](-loadlibrary.md) и [**GetProcAddress**](-getprocaddress-.md) для динамической привязки к Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="c4796-118">You can also use the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4796-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c4796-119">Requirements</span></span>



| <span data-ttu-id="c4796-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c4796-120">Requirement</span></span> | <span data-ttu-id="c4796-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c4796-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c4796-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c4796-122">DLL</span></span><br/> | <dl> <span data-ttu-id="c4796-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4796-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




