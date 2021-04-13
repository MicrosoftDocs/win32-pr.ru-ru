---
description: Используется с \_ \_ свойством политики ПОЛЬЗОВАТЕЛЬСКОГО интерфейса NCRYPT \_ для хранения сведений о пользовательском интерфейсе для ключа.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Структура NCRYPT_UI_POLICY_BLOB (NCrypt \_ provider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544994"
---
# <a name="ncrypt_ui_policy_blob-structure"></a><span data-ttu-id="c1d57-103">\_ \_ \_ Структура большого двоичного объекта политики пользовательского интерфейса NCRYPT</span><span class="sxs-lookup"><span data-stu-id="c1d57-103">NCRYPT\_UI\_POLICY\_BLOB structure</span></span>

<span data-ttu-id="c1d57-104">Структура **\_ \_ \_ больших двоичных объектов политики пользовательского интерфейса NCrypt** используется со свойством [**\_ \_ \_ Свойства политики пользовательского интерфейса NCrypt**](key-storage-property-identifiers.md) для хранения сведений о пользовательском интерфейсе для ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-104">The **NCRYPT\_UI\_POLICY\_BLOB** structure is used with the [**NCRYPT\_UI\_POLICY\_PROPERTY**](key-storage-property-identifiers.md) property to contain user interface information for a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d57-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c1d57-105">Syntax</span></span>


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a><span data-ttu-id="c1d57-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c1d57-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c1d57-107">**двверсион**</span><span class="sxs-lookup"><span data-stu-id="c1d57-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c1d57-108">Номер версии структуры.</span><span class="sxs-lookup"><span data-stu-id="c1d57-108">The version number of the structure.</span></span> <span data-ttu-id="c1d57-109">Этот элемент должен содержать 1.</span><span class="sxs-lookup"><span data-stu-id="c1d57-109">This member must contain 1.</span></span>

</dd> <dt>

<span data-ttu-id="c1d57-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="c1d57-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c1d57-111">Набор флагов, предоставляющих дополнительные сведения о пользовательском интерфейсе или требования.</span><span class="sxs-lookup"><span data-stu-id="c1d57-111">A set of flags that provide additional user interface information or requirements.</span></span>



| <span data-ttu-id="c1d57-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c1d57-112">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="c1d57-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c1d57-113">Meaning</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <span data-ttu-id="c1d57-114"><dt>**NCRYPT \_ \_ \_ \_ Флаг ключа защиты пользовательского интерфейса**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="c1d57-114"><dt>**NCRYPT\_UI\_PROTECT\_KEY\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="c1d57-115">При необходимости Отобразите пользовательский интерфейс строгого ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-115">Display the strong key user interface as needed.</span></span><br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <span data-ttu-id="c1d57-116"><dt>**NCRYPT \_ \_ \_ Флаг высокого уровня \_ защиты \_ пользовательского интерфейса**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="c1d57-116"><dt>**NCRYPT\_UI\_FORCE\_HIGH\_PROTECTION\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="c1d57-117">Принудительная высокая защита.</span><span class="sxs-lookup"><span data-stu-id="c1d57-117">Force high protection.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="c1d57-118">**кбкреатионтитле**</span><span class="sxs-lookup"><span data-stu-id="c1d57-118">**cbCreationTitle**</span></span>
</dt> <dd>

<span data-ttu-id="c1d57-119">Длина заголовка создания в байтах.</span><span class="sxs-lookup"><span data-stu-id="c1d57-119">The length, in bytes, of the creation title.</span></span> <span data-ttu-id="c1d57-120">Заголовок создания — это строка в Юникоде, заканчивающаяся нулем, которая указывает текст, используемый в качестве заголовка диалогового окна строгого ключа после завершения работы ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-120">The creation title is a null-terminated Unicode string that specifies the text that is used as the title of the strong key dialog box when the key is completed.</span></span> <span data-ttu-id="c1d57-121">Заголовок создания необходимо поместить сразу после структуры **\_ \_ \_ большого двоичного объекта политики пользовательского интерфейса NCRYPT** .</span><span class="sxs-lookup"><span data-stu-id="c1d57-121">The creation title must be placed immediately following the **NCRYPT\_UI\_POLICY\_BLOB** structure.</span></span> <span data-ttu-id="c1d57-122">Если значение элемента **кбкреатионтитле** равно 0, в заголовке диалогового окна строгого ключа используется заголовок создания по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1d57-122">If the value of the **cbCreationTitle** member is set to 0, a default creation title is used for the title of the strong key dialog box.</span></span> <span data-ttu-id="c1d57-123">Этот элемент используется только для финализации ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-123">This member is only used on key finalization.</span></span>

</dd> <dt>

<span data-ttu-id="c1d57-124">**кбфриендлинаме**</span><span class="sxs-lookup"><span data-stu-id="c1d57-124">**cbFriendlyName**</span></span>
</dt> <dd>

<span data-ttu-id="c1d57-125">Длина понятного имени ключа в байтах.</span><span class="sxs-lookup"><span data-stu-id="c1d57-125">The length, in bytes, of the friendly name of the key.</span></span> <span data-ttu-id="c1d57-126">Понятное имя — это строка в Юникоде, заканчивающаяся нулем, которая содержит текст, отображаемый в диалоговом окне надежный ключ в качестве имени ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-126">The friendly name is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the name of the key.</span></span> <span data-ttu-id="c1d57-127">Понятное имя должно располагаться сразу после заголовка создания в этом большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="c1d57-127">The friendly name must be placed immediately following the creation title in this BLOB.</span></span> <span data-ttu-id="c1d57-128">Если для элемента **кбфриендлинаме** задано значение 0, в диалоговом окне надежный ключ используется имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1d57-128">If the value of the **cbFriendlyName** member is set to 0, a default name is used in the strong key dialog box.</span></span> <span data-ttu-id="c1d57-129">Этот элемент используется как при завершении ключа, так и при использовании ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-129">This member is used both when the key is completed and when the key is used.</span></span>

</dd> <dt>

<span data-ttu-id="c1d57-130">**кбдескриптион**</span><span class="sxs-lookup"><span data-stu-id="c1d57-130">**cbDescription**</span></span>
</dt> <dd>

<span data-ttu-id="c1d57-131">Длина (в байтах) ключевого описания.</span><span class="sxs-lookup"><span data-stu-id="c1d57-131">The length, in bytes, of the key description.</span></span> <span data-ttu-id="c1d57-132">Ключевое описание — это строка в Юникоде, заканчивающаяся нулем и содержащая текст, который отображается в диалоговом окне строгое ключевое поле в качестве описания ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-132">The key description is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the description of the key.</span></span> <span data-ttu-id="c1d57-133">Значение описания должно располагаться сразу после понятного имени в этом большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="c1d57-133">The description value must be placed immediately following the friendly name in this BLOB.</span></span> <span data-ttu-id="c1d57-134">Если значение элемента **кбдескриптион** равно 0, в диалоговом окне надежный ключ используется описание по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1d57-134">If the value of the **cbDescription** member is set to 0, a default description is used in the strong key dialog box.</span></span> <span data-ttu-id="c1d57-135">Этот элемент используется как при завершении ключа, так и при использовании ключа.</span><span class="sxs-lookup"><span data-stu-id="c1d57-135">This member is used both when the key is completed and when the key is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c1d57-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1d57-136">Remarks</span></span>

<span data-ttu-id="c1d57-137">Эта структура содержится в \_ заголовке NCrypt provider. h.</span><span class="sxs-lookup"><span data-stu-id="c1d57-137">This structure is included in the Ncrypt\_provider.h header.</span></span> <span data-ttu-id="c1d57-138">Чтобы использовать структуру, необходимо загрузить [пакет средств разработки поставщика служб шифрования](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) из Microsoft Connect.</span><span class="sxs-lookup"><span data-stu-id="c1d57-138">To use the structure, you must download the [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) from Microsoft Connect.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d57-139">Требования</span><span class="sxs-lookup"><span data-stu-id="c1d57-139">Requirements</span></span>



| <span data-ttu-id="c1d57-140">Требование</span><span class="sxs-lookup"><span data-stu-id="c1d57-140">Requirement</span></span> | <span data-ttu-id="c1d57-141">Значение</span><span class="sxs-lookup"><span data-stu-id="c1d57-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d57-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1d57-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d57-143">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1d57-143">Windows Vista \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c1d57-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1d57-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d57-145">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1d57-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c1d57-146">Header</span><span class="sxs-lookup"><span data-stu-id="c1d57-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1d57-147"><dt>NCrypt \_ provider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1d57-147"><dt>Ncrypt\_provider.h</dt></span></span> </dl> |



 

