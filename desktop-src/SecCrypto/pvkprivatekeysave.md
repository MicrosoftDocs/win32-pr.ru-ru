---
description: Сохраняет закрытый ключ и соответствующий открытый ключ в указанном файле.
ms.assetid: 491a128a-b4aa-4cca-a835-d0e8d7df6720
title: Функция Пвкприватекэйсаве
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeySave
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: ef60c3f615a704248fbcb8630322fa6b598141ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683942"
---
# <a name="pvkprivatekeysave-function"></a><span data-ttu-id="b40d3-103">Функция Пвкприватекэйсаве</span><span class="sxs-lookup"><span data-stu-id="b40d3-103">PvkPrivateKeySave function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b40d3-104">Это нерекомендуемый API.</span><span class="sxs-lookup"><span data-stu-id="b40d3-104">This API is deprecated.</span></span> <span data-ttu-id="b40d3-105">Корпорация Майкрософт может удалить этот API в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="b40d3-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="b40d3-106">Функция **пвкприватекэйсаве** сохраняет [*закрытый ключ*](../secgloss/p-gly.md) и соответствующий [*открытый ключ*](../secgloss/p-gly.md) в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="b40d3-106">The **PvkPrivateKeySave** function saves a [*private key*](../secgloss/p-gly.md) and its corresponding [*public key*](../secgloss/p-gly.md) to a specified file.</span></span>

> [!Note]  
> <span data-ttu-id="b40d3-107">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="b40d3-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="b40d3-108">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="b40d3-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b40d3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b40d3-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeySave(
  _In_ HCRYPTPROV hCryptProv,
  _In_ HANDLE     hFile,
  _In_ DWORD      dwKeySpec,
  _In_ HWND       hwndOwner,
  _In_ LPCWSTR    pwszKeyName,
  _In_ DWORD      dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b40d3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b40d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b40d3-111">*хкриптпров* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-111">*hCryptProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40d3-112">Маркер [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="b40d3-112">A handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

</dd> <dt>

<span data-ttu-id="b40d3-113">*hFile* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-113">*hFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40d3-114">Маркер файла, созданного с помощью начального разрешения на чтение и запись и последующее разрешение только на чтение.</span><span class="sxs-lookup"><span data-stu-id="b40d3-114">A handle to a file created with initial read/write permission and subsequent read-only permission.</span></span>

</dd> <dt>

<span data-ttu-id="b40d3-115">*двкэйспек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-115">*dwKeySpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40d3-116">Длинное целое число для типа ключа.</span><span class="sxs-lookup"><span data-stu-id="b40d3-116">A long integer for the type of key.</span></span> <span data-ttu-id="b40d3-117">Возможные значения: **в \_ Кэйексчанже** или **в \_ сигнатуре**.</span><span class="sxs-lookup"><span data-stu-id="b40d3-117">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="b40d3-118">*хвндовнер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-118">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40d3-119">Если для шифрования закрытого ключа требуется пароль, этот параметр является маркером родителя диалогового окна; в противном случае он имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b40d3-119">If a password is required to encrypt the private key, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b40d3-120">*пвсзкэйнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-120">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40d3-121">Указатель на строку, завершающуюся нулем, для имени сохраняемого ключа.</span><span class="sxs-lookup"><span data-stu-id="b40d3-121">A pointer to a null-terminated string for the name of the key to be saved.</span></span>

</dd> <dt>

<span data-ttu-id="b40d3-122">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b40d3-123">Значение **типа DWORD** , указывающее дополнительные параметры для функции.</span><span class="sxs-lookup"><span data-stu-id="b40d3-123">A **DWORD** value that specifies additional options for the function.</span></span> <span data-ttu-id="b40d3-124">Дополнительные сведения см. в описании параметра *dwFlags* в [**криптекспорткэй**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="b40d3-124">For more information, see the *dwFlags* parameter in [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b40d3-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b40d3-125">Return value</span></span>

<span data-ttu-id="b40d3-126">При успешном выполнении эта функция возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="b40d3-126">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="b40d3-127">Функция **пвкприватекэйсаве** возвращает **значение false** в случае сбоя.</span><span class="sxs-lookup"><span data-stu-id="b40d3-127">The **PvkPrivateKeySave** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="b40d3-128">Требования</span><span class="sxs-lookup"><span data-stu-id="b40d3-128">Requirements</span></span>



| <span data-ttu-id="b40d3-129">Требование</span><span class="sxs-lookup"><span data-stu-id="b40d3-129">Requirement</span></span> | <span data-ttu-id="b40d3-130">Значение</span><span class="sxs-lookup"><span data-stu-id="b40d3-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b40d3-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b40d3-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b40d3-132">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="b40d3-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b40d3-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b40d3-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b40d3-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b40d3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b40d3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b40d3-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b40d3-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
