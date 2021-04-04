---
description: Задает атрибуты для подписи Authenticode.
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: Структура SIGNER_ATTR_AUTHCODE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999658"
---
# <a name="signer_attr_authcode-structure"></a><span data-ttu-id="8bdd9-103">Двухфакторной, подпись \_ attr, \_ Структура</span><span class="sxs-lookup"><span data-stu-id="8bdd9-103">SIGNER\_ATTR\_AUTHCODE structure</span></span>

<span data-ttu-id="8bdd9-104">**\_ \_ Двухфакторнойная структура attr** определяет атрибуты для подписи [*Authenticode*](../secgloss/a-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="8bdd9-104">The **SIGNER\_ATTR\_AUTHCODE** structure specifies attributes for an [*Authenticode*](../secgloss/a-gly.md) signature.</span></span>

> [!Note]  
> <span data-ttu-id="8bdd9-105">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="8bdd9-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="8bdd9-106">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="8bdd9-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8bdd9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8bdd9-107">Syntax</span></span>


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a><span data-ttu-id="8bdd9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8bdd9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8bdd9-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="8bdd9-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="8bdd9-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="8bdd9-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="8bdd9-111">**фкоммерЦиал**</span><span class="sxs-lookup"><span data-stu-id="8bdd9-111">**fCommercial**</span></span>
</dt> <dd>

<span data-ttu-id="8bdd9-112">**Значение true** , чтобы подписать субъект в качестве коммерческого издателя; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8bdd9-112">**TRUE** to sign the subject as a commercial publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8bdd9-113">**финдивидуал**</span><span class="sxs-lookup"><span data-stu-id="8bdd9-113">**fIndividual**</span></span>
</dt> <dd>

<span data-ttu-id="8bdd9-114">**Значение true** , чтобы подписать тему как отдельный издатель; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="8bdd9-114">**TRUE** to sign the subject as an individual publisher; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="8bdd9-115">**pwszName**</span><span class="sxs-lookup"><span data-stu-id="8bdd9-115">**pwszName**</span></span>
</dt> <dd>

<span data-ttu-id="8bdd9-116">Отображаемое имя файла при скачивании.</span><span class="sxs-lookup"><span data-stu-id="8bdd9-116">The display name of the file upon download.</span></span>

</dd> <dt>

<span data-ttu-id="8bdd9-117">**пвсзинфо**</span><span class="sxs-lookup"><span data-stu-id="8bdd9-117">**pwszInfo**</span></span>
</dt> <dd>

<span data-ttu-id="8bdd9-118">Отображаемое имя URL-адреса файла при скачивании.</span><span class="sxs-lookup"><span data-stu-id="8bdd9-118">The display name of the URL of the file upon download.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8bdd9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8bdd9-119">Requirements</span></span>



| <span data-ttu-id="8bdd9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8bdd9-120">Requirement</span></span> | <span data-ttu-id="8bdd9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8bdd9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8bdd9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8bdd9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8bdd9-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8bdd9-123">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8bdd9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8bdd9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8bdd9-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8bdd9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bdd9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8bdd9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bdd9-127">**\_сведения о подписи ПОДписывания \_**</span><span class="sxs-lookup"><span data-stu-id="8bdd9-127">**SIGNER\_SIGNATURE\_INFO**</span></span>](signer-signature-info.md)
</dt> </dl>

 

 
