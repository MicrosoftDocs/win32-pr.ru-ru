---
description: Задает размер блока Clear (незашифрованный) байт для шифрования шаблона на основе образца.
ms.assetid: F65112FA-B380-45F8-A1FC-3408FE6E49E2
title: Атрибут MFSampleExtension_Encryption_SkipByteBlock (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18003c03df7e65314846d34cb1d1093f5b2507a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898738"
---
# <a name="mfsampleextension_encryption_skipbyteblock-attribute"></a><span data-ttu-id="db6b1-103">\_ \_ Атрибут Скипбитеблокк Encryption мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="db6b1-103">MFSampleExtension\_Encryption\_SkipByteBlock attribute</span></span>

<span data-ttu-id="db6b1-104">Задает размер блока Clear (незашифрованный) байт для шифрования шаблона на основе образца.</span><span class="sxs-lookup"><span data-stu-id="db6b1-104">Specifies the clear (non-encrypted) byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="db6b1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="db6b1-105">Data type</span></span>

<span data-ttu-id="db6b1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="db6b1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="db6b1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db6b1-107">Remarks</span></span>

<span data-ttu-id="db6b1-108">Число зашифрованных байтов в блоке сопоставления подобразца указывается в атрибуте [мфсампликстенсион \_ ENCRYPTION \_ криптбитеблокк](mfsampleextension-encryption-cryptbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="db6b1-108">The number of encrypted bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) attribute.</span></span> <span data-ttu-id="db6b1-109">Если один из этих атрибутов отсутствует или имеет значение 0, это означает, что образец данных не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="db6b1-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="db6b1-110">Оба этих значения должны быть ненулевыми, положительные значения или оба должны иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="db6b1-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="db6b1-111">В случаях, когда источником является формат MP4, значение задается на основе значений блока "пропустить байт" по умолчанию в \_ \_ \_ поле "Track Encryption" ("ТЕНК") в заголовке MP4.</span><span class="sxs-lookup"><span data-stu-id="db6b1-111">In cases where the Source is MP4-based, the value is set based off the values of default\_skip\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="db6b1-112">Дополнительные сведения см. в разделе [мфсампликстенсион \_ ENCRYPTION \_ протектионсчеме](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="db6b1-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db6b1-113">Требования</span><span class="sxs-lookup"><span data-stu-id="db6b1-113">Requirements</span></span>



| <span data-ttu-id="db6b1-114">Требование</span><span class="sxs-lookup"><span data-stu-id="db6b1-114">Requirement</span></span> | <span data-ttu-id="db6b1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="db6b1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db6b1-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db6b1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db6b1-117">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="db6b1-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="db6b1-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db6b1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db6b1-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="db6b1-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="db6b1-120">Header</span><span class="sxs-lookup"><span data-stu-id="db6b1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6b1-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6b1-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




