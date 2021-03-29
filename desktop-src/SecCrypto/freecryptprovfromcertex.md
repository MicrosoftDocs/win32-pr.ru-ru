---
description: 'Освобождает дескриптор от поставщика служб шифрования (CSP) или ключа API шифрования: следующего поколения (CNG).'
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: Функция Фрикриптпровфромцертекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912039"
---
# <a name="freecryptprovfromcertex-function"></a><span data-ttu-id="4561a-103">Функция Фрикриптпровфромцертекс</span><span class="sxs-lookup"><span data-stu-id="4561a-103">FreeCryptProvFromCertEx function</span></span>

<span data-ttu-id="4561a-104">Функция **фрикриптпровфромцертекс** освобождает дескриптор как [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP), так и ключ API шифрования: следующего поколения (CNG).</span><span class="sxs-lookup"><span data-stu-id="4561a-104">The **FreeCryptProvFromCertEx** function releases the handle either to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or to a Cryptography API: Next Generation (CNG) key.</span></span>

> [!Note]  
> <span data-ttu-id="4561a-105">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="4561a-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="4561a-106">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="4561a-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4561a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4561a-107">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="4561a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4561a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4561a-109">*факкуиред* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4561a-109">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4561a-110">Значение типа, указывающее, был ли получен обработчик поставщика из [*сертификата*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4561a-110">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="4561a-111">*хпров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4561a-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4561a-112">Описатель для CSP или маркера для ключа CNG.</span><span class="sxs-lookup"><span data-stu-id="4561a-112">A handle to a CAPICOM CSP or a handle to a CNG key.</span></span>

</dd> <dt>

<span data-ttu-id="4561a-113">*двкэйспек*</span><span class="sxs-lookup"><span data-stu-id="4561a-113">*dwKeySpec*</span></span> 
</dt> <dd>

<span data-ttu-id="4561a-114">Адрес переменной **типа DWORD** , которая получает дополнительные сведения о ключе.</span><span class="sxs-lookup"><span data-stu-id="4561a-114">The address of a **DWORD** variable that receives additional information about the key.</span></span> <span data-ttu-id="4561a-115">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="4561a-115">This can be one of the following values.</span></span>



| <span data-ttu-id="4561a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4561a-116">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="4561a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4561a-117">Meaning</span></span>                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="4561a-118"><dt>**по адресу \_ кэйексчанже**</dt></span><span class="sxs-lookup"><span data-stu-id="4561a-118"><dt>**AT\_KEYEXCHANGE**</dt></span></span> </dl>                     | <span data-ttu-id="4561a-119">Пара ключей является парой обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="4561a-119">The key pair is a key exchange pair.</span></span><br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="4561a-120"><dt>**в \_ сигнатуре**</dt></span><span class="sxs-lookup"><span data-stu-id="4561a-120"><dt>**AT\_SIGNATURE**</dt></span></span> </dl>                           | <span data-ttu-id="4561a-121">Пара ключей является парой сигнатур.</span><span class="sxs-lookup"><span data-stu-id="4561a-121">The key pair is a signature pair.</span></span><br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <span data-ttu-id="4561a-122"><dt>**\_ \_ Спецификация ключа NCRYPT для сертификата \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4561a-122"><dt>**CERT\_NCRYPT\_KEY\_SPEC**</dt></span></span> </dl> | <span data-ttu-id="4561a-123">Ключ является ключом CNG.</span><span class="sxs-lookup"><span data-stu-id="4561a-123">The key is a CNG key.</span></span><br/> <span data-ttu-id="4561a-124">**Windows Server 2003 и Windows XP:** Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="4561a-124">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4561a-125">*пвсзкапипровидер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4561a-125">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4561a-126">Указатель на строку, завершающуюся нулем, для имени поставщика.</span><span class="sxs-lookup"><span data-stu-id="4561a-126">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="4561a-127">*двпровидертипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4561a-127">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4561a-128">Указывает тип CSP.</span><span class="sxs-lookup"><span data-stu-id="4561a-128">Specifies the CSP type.</span></span> <span data-ttu-id="4561a-129">Это может быть ноль или один из [типов поставщиков служб шифрования](cryptographic-provider-types.md).</span><span class="sxs-lookup"><span data-stu-id="4561a-129">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="4561a-130">Если этот член равен нулю, контейнер ключей является одним из поставщиков хранилища ключей CNG.</span><span class="sxs-lookup"><span data-stu-id="4561a-130">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="4561a-131">*пвсзтмпконтаинер* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="4561a-131">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4561a-132">Указатель на строку, завершающуюся нулем, для имени временного контейнера ключей.</span><span class="sxs-lookup"><span data-stu-id="4561a-132">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4561a-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4561a-133">Return value</span></span>

<span data-ttu-id="4561a-134">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4561a-134">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4561a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="4561a-135">Requirements</span></span>



| <span data-ttu-id="4561a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="4561a-136">Requirement</span></span> | <span data-ttu-id="4561a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="4561a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4561a-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4561a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4561a-139">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4561a-139">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4561a-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4561a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4561a-141">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4561a-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4561a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4561a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4561a-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4561a-143"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
