---
description: Освобождает дескриптор поставщика служб шифрования (CSP) и при необходимости удаляет временный контейнер, созданный функцией Пвкжеткриптпров.
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: Функция Пвкфрикриптпров
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684334"
---
# <a name="pvkfreecryptprov-function"></a><span data-ttu-id="a7fec-103">Функция Пвкфрикриптпров</span><span class="sxs-lookup"><span data-stu-id="a7fec-103">PvkFreeCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7fec-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="a7fec-104">This API is deprecated.</span></span> <span data-ttu-id="a7fec-105">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="a7fec-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="a7fec-106">Функция **пвкфрикриптпров** освобождает дескриптор [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и при необходимости удаляет временный контейнер, созданный функцией [**пвкжеткриптпров**](pvkgetcryptprov.md) .</span><span class="sxs-lookup"><span data-stu-id="a7fec-106">The **PvkFreeCryptProv** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**PvkGetCryptProv**](pvkgetcryptprov.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="a7fec-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="a7fec-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="a7fec-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="a7fec-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a7fec-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7fec-109">Syntax</span></span>


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="a7fec-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a7fec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fec-111">*хпров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7fec-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fec-112">Маркер для CSP.</span><span class="sxs-lookup"><span data-stu-id="a7fec-112">A handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="a7fec-113">*пвсзкапипровидер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7fec-113">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fec-114">Указатель на строку, завершающуюся нулем, для имени CSP.</span><span class="sxs-lookup"><span data-stu-id="a7fec-114">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="a7fec-115">*двпровидертипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a7fec-115">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fec-116">Значение типа **DWORD** , представляющее тип поставщика служб шифрования.</span><span class="sxs-lookup"><span data-stu-id="a7fec-116">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="a7fec-117">Дополнительные сведения см. в разделе [типы поставщиков служб шифрования](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="a7fec-117">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="a7fec-118">*пвсзтмпконтаинер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="a7fec-118">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fec-119">Указатель на строку, завершающуюся нулем, для имени контейнера временного ключа.</span><span class="sxs-lookup"><span data-stu-id="a7fec-119">A pointer to a null-terminated string for the temporary key container name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7fec-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a7fec-120">Return value</span></span>

<span data-ttu-id="a7fec-121">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a7fec-121">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7fec-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a7fec-122">Requirements</span></span>



| <span data-ttu-id="a7fec-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a7fec-123">Requirement</span></span> | <span data-ttu-id="a7fec-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a7fec-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7fec-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a7fec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a7fec-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a7fec-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a7fec-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a7fec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a7fec-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7fec-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7fec-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a7fec-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7fec-130"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7fec-130"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
