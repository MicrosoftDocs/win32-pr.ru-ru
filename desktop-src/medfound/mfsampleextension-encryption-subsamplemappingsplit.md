---
description: Задает сопоставление подобразца для образца, указывающего очищенные и зашифрованные байты в образце данных.
ms.assetid: E672F53D-2083-430B-90D2-A1DA482EF9E1
title: Атрибут MFSampleExtension_Encryption_SubSampleMappingSplit (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c90fb6ae22417f059bfa3268382877363178940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719427"
---
# <a name="mfsampleextension_encryption_subsamplemappingsplit-attribute"></a><span data-ttu-id="80b75-103">\_ \_ Атрибут Субсамплемаппингсплит Encryption мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="80b75-103">MFSampleExtension\_Encryption\_SubSampleMappingSplit attribute</span></span>

<span data-ttu-id="80b75-104">Задает сопоставление подобразца для образца, указывающего очищенные и зашифрованные байты в образце данных.</span><span class="sxs-lookup"><span data-stu-id="80b75-104">Sets the sub-sample mapping for the sample indicating the clear and encrypted bytes in the sample data.</span></span>

## <a name="data-type"></a><span data-ttu-id="80b75-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="80b75-105">Data type</span></span>

<span data-ttu-id="80b75-106">**ОБЪЕКТЕ**</span><span class="sxs-lookup"><span data-stu-id="80b75-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="80b75-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80b75-107">Remarks</span></span>

<span data-ttu-id="80b75-108">**Большой двоичный объект** должен содержать массив диапазонов байтов в виде DWORD, где каждый из двух значений DWORD делает набор.</span><span class="sxs-lookup"><span data-stu-id="80b75-108">The **BLOB** should contain an array of byte ranges as DWORDs where every two DWORDs makes a set.</span></span> <span data-ttu-id="80b75-109">Первый DWORD в каждом наборе — это число байтов очистки, а второй DWORD набора — число зашифрованных байтов.</span><span class="sxs-lookup"><span data-stu-id="80b75-109">The first DWORD in each set is the number of clear bytes and the second DWORD of the set is the number of encrypted bytes.</span></span> <span data-ttu-id="80b75-110">Обратите внимание, что пара нулей не является допустимым набором (любое значение может быть равно 0, но не одновременно).</span><span class="sxs-lookup"><span data-stu-id="80b75-110">Note that a pair of 0s is not a valid set (either value can be 0, but not both).</span></span> <span data-ttu-id="80b75-111">Массив диапазонов байтов указывает, какие диапазоны следует расшифровывать, в том числе возможность дешифрования всего образца.</span><span class="sxs-lookup"><span data-stu-id="80b75-111">The array of byte ranges indicate which ranges to decrypt, including the possibility that the entire sample should not be decrypted.</span></span> <span data-ttu-id="80b75-112">Не рекомендуется устанавливать этот параметр в Clear Samples, хотя можно добиться того же результата, задав для него соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="80b75-112">It is recommended that this should not be set on clear samples, though it is possible to achieve the same result by setting it with the appropriate values.</span></span>

## <a name="examples"></a><span data-ttu-id="80b75-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="80b75-113">Examples</span></span>

<span data-ttu-id="80b75-114">В следующем примере показано, как задать \_ субсамплемаппингсплит шифрования мфсампликстенсион \_ .</span><span class="sxs-lookup"><span data-stu-id="80b75-114">The following example shows how to set MFSampleExtension\_Encryption\_SubSampleMappingSplit.</span></span>


```C++
// m_spSample is a IMFSample
// pdwSubSampleMap is a DWORD*
// dwSubSampleMapSize is a DWORD

m_spSample->SetBlob( MFSampleExtension_Encryption_SubSampleMappingSplit,
                    (BYTE*)pdwSubSampleMap, 
                    dwSubSampleMapSize * sizeof(DWORD) );
```



## <a name="requirements"></a><span data-ttu-id="80b75-115">Требования</span><span class="sxs-lookup"><span data-stu-id="80b75-115">Requirements</span></span>



| <span data-ttu-id="80b75-116">Требование</span><span class="sxs-lookup"><span data-stu-id="80b75-116">Requirement</span></span> | <span data-ttu-id="80b75-117">Значение</span><span class="sxs-lookup"><span data-stu-id="80b75-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="80b75-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="80b75-118">Minimum supported client</span></span><br/> | <span data-ttu-id="80b75-119">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="80b75-119">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="80b75-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="80b75-120">Minimum supported server</span></span><br/> | <span data-ttu-id="80b75-121">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="80b75-121">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="80b75-122">Header</span><span class="sxs-lookup"><span data-stu-id="80b75-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="80b75-123"><dt>Мфапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="80b75-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b75-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="80b75-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b75-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="80b75-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="80b75-126">**имфсампле**</span><span class="sxs-lookup"><span data-stu-id="80b75-126">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="80b75-127">\_KeyID содержимого \_ мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="80b75-127">MFSampleExtension\_Content\_KeyID</span></span>](mfsampleextension-content-keyid.md)
</dt> </dl>

 

 




