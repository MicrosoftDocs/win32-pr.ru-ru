---
description: Указывает файл для подписи.
ms.assetid: 5b45d855-ede8-43eb-9253-e3fe1716686b
title: Структура SIGNER_FILE_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_FILE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 71e7c360d0034d9435386cf31579299c6d047131
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664386"
---
# <a name="signer_file_info-structure"></a><span data-ttu-id="b311b-103">\_ \_ Структура сведений о файле подписывания</span><span class="sxs-lookup"><span data-stu-id="b311b-103">SIGNER\_FILE\_INFO structure</span></span>

<span data-ttu-id="b311b-104">Структура **\_ \_ сведений о файле подписывания** указывает файл для подписи.</span><span class="sxs-lookup"><span data-stu-id="b311b-104">The **SIGNER\_FILE\_INFO** structure specifies a file to sign.</span></span>

> [!Note]  
> <span data-ttu-id="b311b-105">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="b311b-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="b311b-106">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="b311b-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b311b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b311b-107">Syntax</span></span>


```C++
typedef struct _SIGNER_FILE_INFO {
  DWORD   cbSize;
  LPCWSTR pwszFileName;
  HANDLE  hFile;
} SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
```



## <a name="members"></a><span data-ttu-id="b311b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b311b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b311b-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="b311b-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="b311b-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="b311b-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="b311b-111">**пвсзфиленаме**</span><span class="sxs-lookup"><span data-stu-id="b311b-111">**pwszFileName**</span></span>
</dt> <dd>

<span data-ttu-id="b311b-112">Указатель на строку, завершающуюся нулем, которая содержит имя файла для подписи.</span><span class="sxs-lookup"><span data-stu-id="b311b-112">A pointer to a null-terminated string that contains the name of the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="b311b-113">**hFile**</span><span class="sxs-lookup"><span data-stu-id="b311b-113">**hFile**</span></span>
</dt> <dd>

<span data-ttu-id="b311b-114">Открытый обработчик для файла, указанного членом **пвсзфиленаме** .</span><span class="sxs-lookup"><span data-stu-id="b311b-114">An open handle to the file specified by the **pwszFileName** member.</span></span> <span data-ttu-id="b311b-115">Если этот член содержит допустимый обработчик, этот маркер используется для доступа к файлу.</span><span class="sxs-lookup"><span data-stu-id="b311b-115">If this member contains a valid handle, this handle is used to access the file.</span></span> <span data-ttu-id="b311b-116">Этому элементу можно присвоить **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b311b-116">This member can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b311b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b311b-117">Requirements</span></span>



| <span data-ttu-id="b311b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b311b-118">Requirement</span></span> | <span data-ttu-id="b311b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b311b-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b311b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b311b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b311b-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b311b-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b311b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b311b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b311b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b311b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b311b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b311b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b311b-125">**\_сведения о субъекте ПОДписывания \_**</span><span class="sxs-lookup"><span data-stu-id="b311b-125">**SIGNER\_SUBJECT\_INFO**</span></span>](signer-subject-info.md)
</dt> </dl>

 

 




