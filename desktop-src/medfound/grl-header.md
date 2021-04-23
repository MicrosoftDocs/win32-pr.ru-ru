---
description: Содержит заголовок глобального списка отзыва (GRL).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Структура GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656093"
---
# <a name="grl_header-structure"></a><span data-ttu-id="55f29-103">\_Структура заголовка GRL</span><span class="sxs-lookup"><span data-stu-id="55f29-103">GRL\_HEADER structure</span></span>

<span data-ttu-id="55f29-104">Содержит заголовок глобального списка отзыва (GRL).</span><span class="sxs-lookup"><span data-stu-id="55f29-104">Contains the global revocation list (GRL) header.</span></span>

## <a name="syntax"></a><span data-ttu-id="55f29-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55f29-105">Syntax</span></span>


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a><span data-ttu-id="55f29-106">Члены</span><span class="sxs-lookup"><span data-stu-id="55f29-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="55f29-107">**всзидентифиер**</span><span class="sxs-lookup"><span data-stu-id="55f29-107">**wszIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-108">Идентификатор GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-108">The GRL identifier.</span></span> <span data-ttu-id="55f29-109">Значение всегда равно L "МСГРЛ".</span><span class="sxs-lookup"><span data-stu-id="55f29-109">The value is always L"MSGRL".</span></span>

</dd> <dt>

<span data-ttu-id="55f29-110">**вформатмажор**</span><span class="sxs-lookup"><span data-stu-id="55f29-110">**wFormatMajor**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-111">Основной номер версии.</span><span class="sxs-lookup"><span data-stu-id="55f29-111">The major version number.</span></span> <span data-ttu-id="55f29-112">В настоящее время значение должно быть равно 1.</span><span class="sxs-lookup"><span data-stu-id="55f29-112">Currently the value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-113">**вформатминор**</span><span class="sxs-lookup"><span data-stu-id="55f29-113">**wFormatMinor**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-114">Дополнительный номер версии.</span><span class="sxs-lookup"><span data-stu-id="55f29-114">The minor version number.</span></span> <span data-ttu-id="55f29-115">В настоящее время значение должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="55f29-115">Currently the value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-116">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="55f29-116">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-117">Значение **fileTime** , указывающее, когда был создан файл.</span><span class="sxs-lookup"><span data-stu-id="55f29-117">A **FILETIME** value that specifies when the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-118">**двсекуенценумбер**</span><span class="sxs-lookup"><span data-stu-id="55f29-118">**dwSequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-119">Номер версии GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-119">The GRL version number.</span></span> <span data-ttu-id="55f29-120">В настоящее время значение должно быть не меньше 3</span><span class="sxs-lookup"><span data-stu-id="55f29-120">Currently the value must be at least 3</span></span>

</dd> <dt>

<span data-ttu-id="55f29-121">**двфорцеребутверсион**</span><span class="sxs-lookup"><span data-stu-id="55f29-121">**dwForceRebootVersion**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-122">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="55f29-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-123">**двфорцепроцессрестартверсион**</span><span class="sxs-lookup"><span data-stu-id="55f29-123">**dwForceProcessRestartVersion**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-124">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="55f29-124">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-125">**кбревокатионсектионоффсет**</span><span class="sxs-lookup"><span data-stu-id="55f29-125">**cbRevocationSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-126">Смещение в байтах от начала GRL до основного раздела.</span><span class="sxs-lookup"><span data-stu-id="55f29-126">The offset, in bytes, from the start of the GRL to the Core section.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-127">**кревокедкернелбинариес**</span><span class="sxs-lookup"><span data-stu-id="55f29-127">**cRevokedKernelBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-128">Число отозванных двоичных файлов ядра, перечисленных в GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-128">The number of revoked kernel binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-129">**кревокедусербинариес**</span><span class="sxs-lookup"><span data-stu-id="55f29-129">**cRevokedUserBinaries**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-130">Число отозванных двоичных файлов пользовательского режима, указанных в GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-130">The number of revoked user-mode binaries listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-131">**кревокедцертификатес**</span><span class="sxs-lookup"><span data-stu-id="55f29-131">**cRevokedCertificates**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-132">Число отозванных сертификатов, перечисленных в GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-132">The number of revoked certificates listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-133">**ктрустедрутс**</span><span class="sxs-lookup"><span data-stu-id="55f29-133">**cTrustedRoots**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-134">Число доверенных корней, перечисленных в GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-134">The number of trusted roots listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-135">**кбекстенсиблесектионоффсет**</span><span class="sxs-lookup"><span data-stu-id="55f29-135">**cbExtensibleSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-136">Смещение в байтах от начала GRL до расширяемого раздела.</span><span class="sxs-lookup"><span data-stu-id="55f29-136">The offset, in bytes, from the start of the GRL to the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-137">**цекстенсиблинтриес**</span><span class="sxs-lookup"><span data-stu-id="55f29-137">**cExtensibleEntries**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-138">Число записей в расширяемом разделе.</span><span class="sxs-lookup"><span data-stu-id="55f29-138">The number of entries in the Extensible section.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-139">**кбреневалсектионоффсет**</span><span class="sxs-lookup"><span data-stu-id="55f29-139">**cbRenewalSectionOffset**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-140">Смещение в байтах от начала GRL до раздела продления.</span><span class="sxs-lookup"><span data-stu-id="55f29-140">The offset, in bytes, from the start of the GRL to the Renewals section.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-141">**кревокедкернелбинариреневалс**</span><span class="sxs-lookup"><span data-stu-id="55f29-141">**cRevokedKernelBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-142">Число двоичных продлений ядра, перечисленных в GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-142">The number of kernel binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-143">**кревокедусербинариреневалс**</span><span class="sxs-lookup"><span data-stu-id="55f29-143">**cRevokedUserBinaryRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-144">Число двоичных продлений пользовательского режима, перечисленных в GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-144">The number of user-mode binary renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-145">**кревокедцертификатереневалс**</span><span class="sxs-lookup"><span data-stu-id="55f29-145">**cRevokedCertificateRenewals**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-146">Число продлений сертификатов, перечисленных в GRL.</span><span class="sxs-lookup"><span data-stu-id="55f29-146">The number of certificate renewals listed in the GRL.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-147">**кбсигнатурекореоффсет**</span><span class="sxs-lookup"><span data-stu-id="55f29-147">**cbSignatureCoreOffset**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-148">Смещение в байтах от начала GRL до базовой сигнатуры раздела.</span><span class="sxs-lookup"><span data-stu-id="55f29-148">The offset, in bytes, from the start of the GRL to the Core section signature.</span></span>

</dd> <dt>

<span data-ttu-id="55f29-149">**кбсигнатурикстоффсет**</span><span class="sxs-lookup"><span data-stu-id="55f29-149">**cbSignatureExtOffset**</span></span>
</dt> <dd>

<span data-ttu-id="55f29-150">Смещение в байтах от начала GRL до сигнатуры расширяемого раздела.</span><span class="sxs-lookup"><span data-stu-id="55f29-150">The offset, in bytes, from the start of the GRL to the Extensible section signature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55f29-151">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55f29-151">Remarks</span></span>

<span data-ttu-id="55f29-152">Все целочисленные значения в GRL имеют прямой порядок байтов.</span><span class="sxs-lookup"><span data-stu-id="55f29-152">All integers in the GRL have little-endian byte ordering.</span></span> <span data-ttu-id="55f29-153">Все структуры вычисляются по 1 байтам.</span><span class="sxs-lookup"><span data-stu-id="55f29-153">All structures are aligned to 1-byte boundaries.</span></span>

<span data-ttu-id="55f29-154">Эта структура не объявлена в заголовке пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="55f29-154">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="55f29-155">Чтобы использовать эту структуру, добавьте приведенное здесь объявление в исходный код.</span><span class="sxs-lookup"><span data-stu-id="55f29-155">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="55f29-156">Требования</span><span class="sxs-lookup"><span data-stu-id="55f29-156">Requirements</span></span>



| <span data-ttu-id="55f29-157">Требование</span><span class="sxs-lookup"><span data-stu-id="55f29-157">Requirement</span></span> | <span data-ttu-id="55f29-158">Значение</span><span class="sxs-lookup"><span data-stu-id="55f29-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55f29-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55f29-159">Minimum supported client</span></span><br/> | <span data-ttu-id="55f29-160">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55f29-160">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55f29-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55f29-161">Minimum supported server</span></span><br/> | <span data-ttu-id="55f29-162">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55f29-162">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55f29-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55f29-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55f29-164">Отзыв сертификата ОПМ</span><span class="sxs-lookup"><span data-stu-id="55f29-164">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="55f29-165">Структуры ОПМ</span><span class="sxs-lookup"><span data-stu-id="55f29-165">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




