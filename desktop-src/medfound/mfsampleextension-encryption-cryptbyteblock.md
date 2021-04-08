---
description: Задает размер зашифрованного блока байтов для шифрования шаблона на основе образца.
ms.assetid: 1F370DEC-20B5-456D-BB68-C94E183410F3
title: Атрибут MFSampleExtension_Encryption_CryptByteBlock (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927e08d81cc8066f73b579c8abf419d754fc1713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080574"
---
# <a name="mfsampleextension_encryption_cryptbyteblock-attribute"></a><span data-ttu-id="3cb31-103">\_ \_ Атрибут Криптбитеблокк Encryption мфсампликстенсион</span><span class="sxs-lookup"><span data-stu-id="3cb31-103">MFSampleExtension\_Encryption\_CryptByteBlock attribute</span></span>

<span data-ttu-id="3cb31-104">Задает размер зашифрованного блока байтов для шифрования шаблона на основе образца.</span><span class="sxs-lookup"><span data-stu-id="3cb31-104">Specifies the encrypted byte block size for sample-based pattern encryption.</span></span>

## <a name="data-type"></a><span data-ttu-id="3cb31-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3cb31-105">Data type</span></span>

<span data-ttu-id="3cb31-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3cb31-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3cb31-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cb31-107">Remarks</span></span>

<span data-ttu-id="3cb31-108">Число четких (незашифрованных) байт в блоке сопоставления подобразца указывается в атрибуте [ \_ \_ скипбитеблокк Encryption мфсампликстенсион](mfsampleextension-encryption-skipbyteblock.md) .</span><span class="sxs-lookup"><span data-stu-id="3cb31-108">The number of clear (non-encrypted) bytes in the subsample mapping block are specified in the [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) attribute.</span></span> <span data-ttu-id="3cb31-109">Если один из этих атрибутов отсутствует или имеет значение 0, это означает, что образец данных не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="3cb31-109">If either of these attributes are not present or have a value of 0, it means that the sample data is not encrypted.</span></span> <span data-ttu-id="3cb31-110">Оба этих значения должны быть ненулевыми, положительные значения или оба должны иметь нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3cb31-110">Either both of these values must be non-zero, positive values, or both must have a value of zero.</span></span>

<span data-ttu-id="3cb31-111">В случаях, когда источником является формат MP4, значение задается на основе значений \_ \_ блока шифрования байтов по умолчанию \_ в поле Track encryption (' ТЕНК ') в заголовке MP4.</span><span class="sxs-lookup"><span data-stu-id="3cb31-111">In cases where the Source is MP4-based, the value is set based off the values of default\_crypt\_byte\_block within the track encryption box (‘tenc’) in the MP4 header.</span></span> <span data-ttu-id="3cb31-112">Дополнительные сведения см. в разделе [мфсампликстенсион \_ ENCRYPTION \_ протектионсчеме](mfsampleextension-encryption-protectionscheme.md).</span><span class="sxs-lookup"><span data-stu-id="3cb31-112">For more information, see [MFSampleExtension\_Encryption\_ProtectionScheme](mfsampleextension-encryption-protectionscheme.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb31-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3cb31-113">Requirements</span></span>



| <span data-ttu-id="3cb31-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3cb31-114">Requirement</span></span> | <span data-ttu-id="3cb31-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3cb31-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb31-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3cb31-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3cb31-117">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="3cb31-117">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3cb31-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3cb31-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3cb31-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3cb31-119">None supported</span></span><br/>                                                          |
| <span data-ttu-id="3cb31-120">Header</span><span class="sxs-lookup"><span data-stu-id="3cb31-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3cb31-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb31-121"><dt>Mfidl.h</dt></span></span> </dl> |



 

 




