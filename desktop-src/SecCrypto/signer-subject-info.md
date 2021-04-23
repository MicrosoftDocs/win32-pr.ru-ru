---
description: Указывает тему для подписи.
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: Структура SIGNER_SUBJECT_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662887"
---
# <a name="signer_subject_info-structure"></a><span data-ttu-id="0838c-103">\_Структура сведений о субъекте ПОДписывания \_</span><span class="sxs-lookup"><span data-stu-id="0838c-103">SIGNER\_SUBJECT\_INFO structure</span></span>

<span data-ttu-id="0838c-104">В структуре **\_ \_ сведений о субъекте-подписывания** указана тема для подписания.</span><span class="sxs-lookup"><span data-stu-id="0838c-104">The **SIGNER\_SUBJECT\_INFO** structure specifies a subject to sign.</span></span>

> [!Note]  
> <span data-ttu-id="0838c-105">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="0838c-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="0838c-106">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0838c-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0838c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0838c-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a><span data-ttu-id="0838c-108">Члены</span><span class="sxs-lookup"><span data-stu-id="0838c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0838c-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="0838c-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="0838c-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="0838c-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="0838c-111">**пдвиндекс**</span><span class="sxs-lookup"><span data-stu-id="0838c-111">**pdwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="0838c-112">Этот член зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="0838c-112">This member is reserved.</span></span> <span data-ttu-id="0838c-113">Он должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="0838c-113">It must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0838c-114">**двсубжектчоице**</span><span class="sxs-lookup"><span data-stu-id="0838c-114">**dwSubjectChoice**</span></span>
</dt> <dd>

<span data-ttu-id="0838c-115">Указывает, является ли субъект файлом или BLOB- [*объектом*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0838c-115">Specifies whether the subject is a file or a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="0838c-116">Этот элемент может иметь одно или несколько следующих значений.</span><span class="sxs-lookup"><span data-stu-id="0838c-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="0838c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0838c-117">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="0838c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0838c-118">Meaning</span></span>                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <span data-ttu-id="0838c-119"><dt>**\_ Подписавший \_BLOB-объект темы**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0838c-119"><dt>**SIGNER\_SUBJECT\_BLOB**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="0838c-120">Субъект — это большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="0838c-120">The subject is a BLOB.</span></span><br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <span data-ttu-id="0838c-121"><dt>**\_ Подписавший \_Файл темы**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0838c-121"><dt>**SIGNER\_SUBJECT\_FILE**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="0838c-122">Субъект — это файл.</span><span class="sxs-lookup"><span data-stu-id="0838c-122">The subject is a file.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0838c-123">**псигнерфилеинфо**</span><span class="sxs-lookup"><span data-stu-id="0838c-123">**pSignerFileInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0838c-124">Указатель на [**\_ \_ информационную структуру файла подписи**](signer-file-info.md) , указывающий файл для подписи.</span><span class="sxs-lookup"><span data-stu-id="0838c-124">A pointer to a [**SIGNER\_FILE\_INFO**](signer-file-info.md) structure that specifies the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="0838c-125">**псигнерблобинфо**</span><span class="sxs-lookup"><span data-stu-id="0838c-125">**pSignerBlobInfo**</span></span>
</dt> <dd>

<span data-ttu-id="0838c-126">Указатель на структуру [**\_ \_ сведений о большом двоичном объекте**](signer-blob-info.md) , указывающий BLOB-объект для подписи.</span><span class="sxs-lookup"><span data-stu-id="0838c-126">A pointer to a [**SIGNER\_BLOB\_INFO**](signer-blob-info.md) structure that specifies the BLOB to sign.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0838c-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0838c-127">Requirements</span></span>



| <span data-ttu-id="0838c-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0838c-128">Requirement</span></span> | <span data-ttu-id="0838c-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0838c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0838c-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0838c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0838c-131">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0838c-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0838c-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0838c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0838c-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0838c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0838c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0838c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0838c-135">**сигнерсигн**</span><span class="sxs-lookup"><span data-stu-id="0838c-135">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="0838c-136">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="0838c-136">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
