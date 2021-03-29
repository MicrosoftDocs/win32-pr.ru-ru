---
description: Освобождает дескриптор поставщика служб шифрования (CSP) и при необходимости удаляет временный контейнер, созданный функцией Жеткриптпровфромцерт.
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: Функция Фрикриптпровфромцерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912040"
---
# <a name="freecryptprovfromcert-function"></a><span data-ttu-id="1721f-103">Функция Фрикриптпровфромцерт</span><span class="sxs-lookup"><span data-stu-id="1721f-103">FreeCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1721f-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="1721f-104">This API is deprecated.</span></span> <span data-ttu-id="1721f-105">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="1721f-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="1721f-106">Функция **фрикриптпровфромцерт** освобождает дескриптор [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP) и при необходимости удаляет временный контейнер, созданный функцией [**жеткриптпровфромцерт**](getcryptprovfromcert.md) .</span><span class="sxs-lookup"><span data-stu-id="1721f-106">The **FreeCryptProvFromCert** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**GetCryptProvFromCert**](getcryptprovfromcert.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="1721f-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="1721f-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="1721f-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="1721f-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1721f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1721f-109">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="1721f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1721f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1721f-111">*факкуиред* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1721f-111">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1721f-112">Значение типа, указывающее, был ли получен обработчик поставщика из [*сертификата*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1721f-112">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="1721f-113">*хпров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1721f-113">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1721f-114">Указатель на структуру [**хкриптпров**](hcryptprov.md) для CSP.</span><span class="sxs-lookup"><span data-stu-id="1721f-114">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="1721f-115">*пвсзкапипровидер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1721f-115">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1721f-116">Указатель на строку, завершающуюся нулем, для имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="1721f-116">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="1721f-117">*двпровидертипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1721f-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1721f-118">Указывает тип CSP.</span><span class="sxs-lookup"><span data-stu-id="1721f-118">Specifies the CSP type.</span></span> <span data-ttu-id="1721f-119">Это может быть ноль или один из [типов поставщиков служб шифрования](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="1721f-119">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="1721f-120">Если этот член равен нулю, контейнер ключей является одним из поставщиков хранилища ключей CNG.</span><span class="sxs-lookup"><span data-stu-id="1721f-120">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="1721f-121">*пвсзтмпконтаинер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="1721f-121">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1721f-122">Указатель на строку, завершающуюся нулем, для имени временного контейнера ключей.</span><span class="sxs-lookup"><span data-stu-id="1721f-122">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1721f-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1721f-123">Return value</span></span>

<span data-ttu-id="1721f-124">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="1721f-124">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1721f-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1721f-125">Requirements</span></span>



| <span data-ttu-id="1721f-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1721f-126">Requirement</span></span> | <span data-ttu-id="1721f-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1721f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1721f-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1721f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1721f-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1721f-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1721f-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1721f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1721f-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1721f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1721f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1721f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1721f-133"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1721f-133"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
