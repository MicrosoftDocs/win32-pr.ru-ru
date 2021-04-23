---
description: Метод Жетфилекапабилитиес извлекает список возможностей файла из текущего файла.
ms.assetid: 0d24efd2-d411-4fb3-95c2-4742a58aeb5e
title: 'Метод Искардфилеакцесс:: Жетфилекапабилитиес'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.GetFileCapabilities
api_type:
- COM
api_location: ''
ms.openlocfilehash: ca22f02d327cdfbea527fba3a87f3f149774c091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265208"
---
# <a name="iscardfileaccessgetfilecapabilities-method"></a><span data-ttu-id="4d717-103">Метод Искардфилеакцесс:: Жетфилекапабилитиес</span><span class="sxs-lookup"><span data-stu-id="4d717-103">ISCardFileAccess::GetFileCapabilities method</span></span>

<span data-ttu-id="4d717-104">\[Метод **жетфилекапабилитиес** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4d717-104">\[The **GetFileCapabilities** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4d717-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4d717-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4d717-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="4d717-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4d717-107">Метод **жетфилекапабилитиес** извлекает список возможностей файла из текущего файла.</span><span class="sxs-lookup"><span data-stu-id="4d717-107">The **GetFileCapabilities** method retrieves a list of file capabilities from the current file.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d717-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d717-108">Syntax</span></span>


```C++
HRESULT GetFileCapabilities(
  [in, out] LPTLV_TABLE *ppProperties,
  [in, out] LONG        *plProperties,
  [in]      SCARD_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="4d717-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d717-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d717-110">*пппропертиес* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4d717-110">*ppProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d717-111">Указатель на TLV-структуры (тег, длина, значение).</span><span class="sxs-lookup"><span data-stu-id="4d717-111">Pointer to TLV (tag, length, value) structures.</span></span> <span data-ttu-id="4d717-112">На входе этот параметр указывает файлы, для которых необходимо получить свойства. в выходных данных этот параметр содержит свойства.</span><span class="sxs-lookup"><span data-stu-id="4d717-112">On input, this parameter indicates the files for which to get properties; on output, this parameter contains the properties.</span></span> <span data-ttu-id="4d717-113">В следующем примере приведено определение структуры TLV.</span><span class="sxs-lookup"><span data-stu-id="4d717-113">The following example is a definition of the TLV structure.</span></span>


```C++
#include <windows.h>

typedef struct
{
  DWORD  Tag;
  DWORD  Length;
  BYTE[]  Value;
  BOOL  Valid;
} TLV;
```



<span data-ttu-id="4d717-114">Дополнительные сведения о структурах TLV см. в разделе [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) .</span><span class="sxs-lookup"><span data-stu-id="4d717-114">For more information on TLV structures, see [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/).</span></span>

</dd> <dt>

<span data-ttu-id="4d717-115">*плпропертиес* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4d717-115">*plProperties* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d717-116">Указатель на число TLV записей в *пппропертиес*.</span><span class="sxs-lookup"><span data-stu-id="4d717-116">Pointer to the number of TLV entries in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="4d717-117">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d717-117">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d717-118">Указывает, следует ли использовать безопасный обмен сообщениями и предварительно выделенные данные.</span><span class="sxs-lookup"><span data-stu-id="4d717-118">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="4d717-119">**\_ \_ Защита \_ обмена сообщениями через SC FL**</span><span class="sxs-lookup"><span data-stu-id="4d717-119">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="4d717-120">**предварительно \_ \_ выделенный SC FL**</span><span class="sxs-lookup"><span data-stu-id="4d717-120">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d717-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d717-121">Return value</span></span>

<span data-ttu-id="4d717-122">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="4d717-122">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4d717-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4d717-123">Return code</span></span>                                                                                   | <span data-ttu-id="4d717-124">Описание</span><span class="sxs-lookup"><span data-stu-id="4d717-124">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4d717-125"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4d717-125"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4d717-126">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="4d717-126">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4d717-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4d717-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4d717-128">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="4d717-128">Invalid parameter.</span></span><br/>                    |
| <dl> <span data-ttu-id="4d717-129"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4d717-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4d717-130">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="4d717-130">A bad pointer was passed in.</span></span><br/>          |
| <dl> <span data-ttu-id="4d717-131"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4d717-131"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4d717-132">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="4d717-132">Out of memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="4d717-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d717-133">Remarks</span></span>

<span data-ttu-id="4d717-134">Список всех методов, определенных этим интерфейсом, см. в разделе [**искардфилеакцесс**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="4d717-134">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="4d717-135">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки [*смарт-карты*](../secgloss/s-gly.md) , если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="4d717-135">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4d717-136">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4d717-136">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d717-137">Требования</span><span class="sxs-lookup"><span data-stu-id="4d717-137">Requirements</span></span>



| <span data-ttu-id="4d717-138">Требование</span><span class="sxs-lookup"><span data-stu-id="4d717-138">Requirement</span></span> | <span data-ttu-id="4d717-139">Значение</span><span class="sxs-lookup"><span data-stu-id="4d717-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4d717-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d717-140">Minimum supported client</span></span><br/> | <span data-ttu-id="4d717-141">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4d717-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4d717-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d717-142">Minimum supported server</span></span><br/> | <span data-ttu-id="4d717-143">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4d717-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4d717-144">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4d717-144">End of client support</span></span><br/>    | <span data-ttu-id="4d717-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4d717-145">Windows XP</span></span><br/>                                |
| <span data-ttu-id="4d717-146">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4d717-146">End of server support</span></span><br/>    | <span data-ttu-id="4d717-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4d717-147">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="4d717-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d717-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d717-149">**искардфилеакцесс**</span><span class="sxs-lookup"><span data-stu-id="4d717-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
