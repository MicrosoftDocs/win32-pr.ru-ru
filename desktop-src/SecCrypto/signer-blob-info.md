---
description: Указывает большой двоичный объект для подписи.
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: Структура SIGNER_BLOB_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a05e99cc4d7fa2eff196159bb449fa7dbfbf3026
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547079"
---
# <a name="signer_blob_info-structure"></a><span data-ttu-id="14f2b-103">\_ \_ Структура сведений о BLOB-объекте подписавши</span><span class="sxs-lookup"><span data-stu-id="14f2b-103">SIGNER\_BLOB\_INFO structure</span></span>

<span data-ttu-id="14f2b-104">\[Структура **\_ \_ сведений о большом двоичном объекте подписавши** доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="14f2b-104">\[The **SIGNER\_BLOB\_INFO** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14f2b-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="14f2b-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="14f2b-106">Структура **\_ \_ сведений о большом двоичном объекте Подписавши** указывает [*большой двоичный объект*](../secgloss/b-gly.md) для подписи.</span><span class="sxs-lookup"><span data-stu-id="14f2b-106">The **SIGNER\_BLOB\_INFO** structure specifies a [*BLOB*](../secgloss/b-gly.md) to sign.</span></span>

> [!Note]  
> <span data-ttu-id="14f2b-107">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="14f2b-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="14f2b-108">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="14f2b-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="14f2b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14f2b-109">Syntax</span></span>


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a><span data-ttu-id="14f2b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="14f2b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="14f2b-111">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="14f2b-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="14f2b-112">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="14f2b-112">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="14f2b-113">**пгуидсубжект**</span><span class="sxs-lookup"><span data-stu-id="14f2b-113">**pGuidSubject**</span></span>
</dt> <dd>

<span data-ttu-id="14f2b-114">Указатель на **идентификатор GUID** , указывающий на загрузку пакета интерфейса субъекта (SIP).</span><span class="sxs-lookup"><span data-stu-id="14f2b-114">A pointer to a **GUID** that specifies the Subject Interface Package (SIP) to load.</span></span>

</dd> <dt>

<span data-ttu-id="14f2b-115">**кбблоб**</span><span class="sxs-lookup"><span data-stu-id="14f2b-115">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="14f2b-116">Размер (в байтах) большого двоичного объекта для подписи.</span><span class="sxs-lookup"><span data-stu-id="14f2b-116">The size, in bytes, of the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="14f2b-117">**пбблоб**</span><span class="sxs-lookup"><span data-stu-id="14f2b-117">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="14f2b-118">Указатель на большой двоичный объект для подписи.</span><span class="sxs-lookup"><span data-stu-id="14f2b-118">A pointer to the BLOB to sign.</span></span>

</dd> <dt>

<span data-ttu-id="14f2b-119">**пвсздисплайнаме**</span><span class="sxs-lookup"><span data-stu-id="14f2b-119">**pwszDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="14f2b-120">Отображаемое имя большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="14f2b-120">The display name of the BLOB.</span></span> <span data-ttu-id="14f2b-121">Этому элементу можно присвоить **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="14f2b-121">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14f2b-122">Требования</span><span class="sxs-lookup"><span data-stu-id="14f2b-122">Requirements</span></span>



| <span data-ttu-id="14f2b-123">Требование</span><span class="sxs-lookup"><span data-stu-id="14f2b-123">Requirement</span></span> | <span data-ttu-id="14f2b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="14f2b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14f2b-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14f2b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="14f2b-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14f2b-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="14f2b-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14f2b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="14f2b-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14f2b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14f2b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14f2b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f2b-130">**\_сведения о субъекте ПОДписывания \_**</span><span class="sxs-lookup"><span data-stu-id="14f2b-130">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 
