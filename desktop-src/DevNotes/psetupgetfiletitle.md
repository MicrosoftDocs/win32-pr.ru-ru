---
description: Возвращает заголовок файла для указанного пути к файлу.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: Функция Псетупжетфилетитле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647977"
---
# <a name="psetupgetfiletitle-function"></a><span data-ttu-id="01798-103">Функция Псетупжетфилетитле</span><span class="sxs-lookup"><span data-stu-id="01798-103">pSetupGetFileTitle function</span></span>

<span data-ttu-id="01798-104">\[Эта функция недоступна в Windows Vista и Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="01798-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="01798-105">Возвращает заголовок файла для указанного пути к файлу.</span><span class="sxs-lookup"><span data-stu-id="01798-105">Retrieves the file title for the specified file path.</span></span>

## <a name="syntax"></a><span data-ttu-id="01798-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01798-106">Syntax</span></span>


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a><span data-ttu-id="01798-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="01798-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01798-108">*Путь к файлу* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="01798-108">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="01798-109">Путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="01798-109">The file path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="01798-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="01798-110">Return value</span></span>

<span data-ttu-id="01798-111">Указатель на строку, которая получает заголовок файла.</span><span class="sxs-lookup"><span data-stu-id="01798-111">A pointer to string that receives the file title.</span></span>

## <a name="remarks"></a><span data-ttu-id="01798-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01798-112">Remarks</span></span>

<span data-ttu-id="01798-113">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="01798-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="01798-114">Требования</span><span class="sxs-lookup"><span data-stu-id="01798-114">Requirements</span></span>



| <span data-ttu-id="01798-115">Требование</span><span class="sxs-lookup"><span data-stu-id="01798-115">Requirement</span></span> | <span data-ttu-id="01798-116">Значение</span><span class="sxs-lookup"><span data-stu-id="01798-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01798-117">DLL</span><span class="sxs-lookup"><span data-stu-id="01798-117">DLL</span></span><br/> | <dl> <span data-ttu-id="01798-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01798-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
