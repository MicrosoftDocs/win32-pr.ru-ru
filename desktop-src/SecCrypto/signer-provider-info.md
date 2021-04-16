---
description: Указывает поставщик служб шифрования (CSP) и сведения о закрытом ключе, используемые для создания цифровой подписи.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Структура SIGNER_PROVIDER_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664103"
---
# <a name="signer_provider_info-structure"></a><span data-ttu-id="823a7-103">\_ \_ Структура сведений о ПОСТАВЩИКе подписи</span><span class="sxs-lookup"><span data-stu-id="823a7-103">SIGNER\_PROVIDER\_INFO structure</span></span>

<span data-ttu-id="823a7-104">В структуре **\_ \_ сведений о поставщике подписи** указан [*поставщик служб шифрования*](../secgloss/c-gly.md) (CSP) и сведения о закрытом ключе, используемые для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="823a7-104">The **SIGNER\_PROVIDER\_INFO** structure specifies the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and private key information used to create a digital signature.</span></span>

> [!Note]  
> <span data-ttu-id="823a7-105">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="823a7-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="823a7-106">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="823a7-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="823a7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="823a7-107">Syntax</span></span>


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a><span data-ttu-id="823a7-108">Члены</span><span class="sxs-lookup"><span data-stu-id="823a7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="823a7-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="823a7-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="823a7-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="823a7-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="823a7-111">**пвсзпровидернаме**</span><span class="sxs-lookup"><span data-stu-id="823a7-111">**pwszProviderName**</span></span>
</dt> <dd>

<span data-ttu-id="823a7-112">Имя CSP, используемого для создания цифровой подписи.</span><span class="sxs-lookup"><span data-stu-id="823a7-112">The name of the CSP used to create the digital signature.</span></span> <span data-ttu-id="823a7-113">Если значение этого элемента равно **null**, используется поставщик по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="823a7-113">If the value of this member is **NULL**, the default provider is used.</span></span>

</dd> <dt>

<span data-ttu-id="823a7-114">**двпровидертипе**</span><span class="sxs-lookup"><span data-stu-id="823a7-114">**dwProviderType**</span></span>
</dt> <dd>

<span data-ttu-id="823a7-115">Тип поставщика служб шифрования, указанный членом **пвсзпровидернаме** .</span><span class="sxs-lookup"><span data-stu-id="823a7-115">The type of the CSP specified by the **pwszProviderName** member.</span></span>

</dd> <dt>

<span data-ttu-id="823a7-116">**двкэйспек**</span><span class="sxs-lookup"><span data-stu-id="823a7-116">**dwKeySpec**</span></span>
</dt> <dd>

<span data-ttu-id="823a7-117">Спецификация ключа.</span><span class="sxs-lookup"><span data-stu-id="823a7-117">The key specification.</span></span> <span data-ttu-id="823a7-118">Если этому члену присвоено значение 0, используется спецификация ключа в члене **пвсзпвкфиленаме** или **пвсзкэйконтаинер** .</span><span class="sxs-lookup"><span data-stu-id="823a7-118">If this member is set to zero, the key specification in the **pwszPvkFileName** or **pwszKeyContainer** member is used.</span></span> <span data-ttu-id="823a7-119">При наличии нескольких ключевых спецификаций в элементе **пвсзкэйконтаинер** используется **\_ сигнатура** .</span><span class="sxs-lookup"><span data-stu-id="823a7-119">If there is more than one key specification in the **pwszKeyContainer** member, **AT\_SIGNATURE** is used.</span></span> <span data-ttu-id="823a7-120">В случае сбоя используется **по адресу \_ кэйексчанже** .</span><span class="sxs-lookup"><span data-stu-id="823a7-120">If it fails, **AT\_KEYEXCHANGE** is used.</span></span>

</dd> <dt>

<span data-ttu-id="823a7-121">**двпвкчоице**</span><span class="sxs-lookup"><span data-stu-id="823a7-121">**dwPvkChoice**</span></span>
</dt> <dd>

<span data-ttu-id="823a7-122">Указывает тип сведений о закрытом ключе.</span><span class="sxs-lookup"><span data-stu-id="823a7-122">Specifies the type of private key information.</span></span> <span data-ttu-id="823a7-123">Этот элемент может иметь одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="823a7-123">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="823a7-124">Значение</span><span class="sxs-lookup"><span data-stu-id="823a7-124">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="823a7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="823a7-125">Meaning</span></span>                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <span data-ttu-id="823a7-126"><dt>**PVK \_ Введите \_ \_ имя файла**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="823a7-126"><dt>**PVK\_TYPE\_FILE\_NAME**</dt> <dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="823a7-127">Сведения о закрытом ключе — это имя файла.</span><span class="sxs-lookup"><span data-stu-id="823a7-127">The private key information is a file name.</span></span><br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <span data-ttu-id="823a7-128"><dt>**PVK \_ Введите \_ keycontainer**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="823a7-128"><dt>**PVK\_TYPE\_KEYCONTAINER**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="823a7-129">Сведения о закрытом ключе являются контейнером ключей.</span><span class="sxs-lookup"><span data-stu-id="823a7-129">The private key information is a key container.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="823a7-130">**пвсзпвкфиленаме**</span><span class="sxs-lookup"><span data-stu-id="823a7-130">**pwszPvkFileName**</span></span>
</dt> <dd>

<span data-ttu-id="823a7-131">Имя файла, содержащего сведения о закрытом ключе.</span><span class="sxs-lookup"><span data-stu-id="823a7-131">The name of the file that contains the private key information.</span></span>

</dd> <dt>

<span data-ttu-id="823a7-132">**пвсзкэйконтаинер**</span><span class="sxs-lookup"><span data-stu-id="823a7-132">**pwszKeyContainer**</span></span>
</dt> <dd>

<span data-ttu-id="823a7-133">Имя контейнера ключей, содержащего сведения о закрытом ключе.</span><span class="sxs-lookup"><span data-stu-id="823a7-133">The name of the key container that contains the private key information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="823a7-134">Требования</span><span class="sxs-lookup"><span data-stu-id="823a7-134">Requirements</span></span>



| <span data-ttu-id="823a7-135">Требование</span><span class="sxs-lookup"><span data-stu-id="823a7-135">Requirement</span></span> | <span data-ttu-id="823a7-136">Значение</span><span class="sxs-lookup"><span data-stu-id="823a7-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="823a7-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="823a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="823a7-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="823a7-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="823a7-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="823a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="823a7-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="823a7-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="823a7-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="823a7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823a7-142">**сигнерсигн**</span><span class="sxs-lookup"><span data-stu-id="823a7-142">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="823a7-143">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="823a7-143">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
