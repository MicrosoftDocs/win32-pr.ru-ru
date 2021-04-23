---
description: Содержит сведения о диалоговом окне, отображаемом функцией Криптуидлгселектцертификате.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Структура CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664478"
---
# <a name="cryptui_selectcertificate_struct-structure"></a><span data-ttu-id="5c9d1-103">\_ \_ Структура структуры динамической компоновки Cryptui селектцертификате</span><span class="sxs-lookup"><span data-stu-id="5c9d1-103">CRYPTUI\_SELECTCERTIFICATE\_STRUCT structure</span></span>

<span data-ttu-id="5c9d1-104">Структура **\_ \_ структуры динамической компоновки Cryptui селектцертификате** содержит сведения о диалоговом окне, отображаемом функцией [**криптуидлгселектцертификате**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-104">The **CRYPTUI\_SELECTCERTIFICATE\_STRUCT** structure contains information about the dialog box displayed by the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9d1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c9d1-105">Syntax</span></span>


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a><span data-ttu-id="5c9d1-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5c9d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c9d1-107">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-108">Размер данной структуры (в байтах).</span><span class="sxs-lookup"><span data-stu-id="5c9d1-108">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-109">**хвндпарент**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-109">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-110">Маркер родительского окна в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-110">The handle of the parent window of the dialog box.</span></span> <span data-ttu-id="5c9d1-111">Если это значение равно **null**, то родительское окно является окном рабочего стола по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-111">If this value is **NULL**, the parent window is the default desktop window.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-113">Задает дополнительные параметры для функции [**криптуидлгселектцертификате**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-113">Specifies additional options for the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span> <span data-ttu-id="5c9d1-114">Это может быть ноль или побитовое **или** для следующих значений.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-114">This can be zero or a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="5c9d1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5c9d1-115">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="5c9d1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5c9d1-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <span data-ttu-id="5c9d1-117"><dt>**ДИНАМИЧЕСКОЙ КОМПОНОВКИ CRYPTUI \_ селектцерт \_ аддфромдс**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-117"><dt>**CRYPTUI\_SELECTCERT\_ADDFROMDS**</dt></span></span> </dl>                              | <span data-ttu-id="5c9d1-118">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-118">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <span data-ttu-id="5c9d1-119"><dt>**ДИНАМИЧЕСКОЙ КОМПОНОВКИ CRYPTUI \_ селектцерт \_ Legacy**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-119"><dt>**CRYPTUI\_SELECTCERT\_LEGACY**</dt></span></span> </dl>                                       | <span data-ttu-id="5c9d1-120">Указывает, что диалоговое окно прежних версий будет отображаться.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-120">Specifies that the legacy dialog is to be displayed.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <span data-ttu-id="5c9d1-121"><dt>**ДИНАМИЧЕСКОЙ КОМПОНОВКИ CRYPTUI \_ селектцерт, \_ выборка**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-121"><dt>**CRYPTUI\_SELECTCERT\_MULTISELECT**</dt></span></span> </dl>                        | <span data-ttu-id="5c9d1-122">Позволяет пользователю выбрать более одного сертификата в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-122">Allows the user to select more than one certificate in the dialog box.</span></span> <span data-ttu-id="5c9d1-123">Если этот флаг установлен, функция [**криптуидлгселектцертификате**](cryptuidlgselectcertificate.md) всегда возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-123">If this flag is set, the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function always returns **NULL**.</span></span> <span data-ttu-id="5c9d1-124">Элемент **хселектедцертсторе** этой структуры должен содержать маркер хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-124">The **hSelectedCertStore** member of this structure must contain a handle to a certificate store.</span></span> <span data-ttu-id="5c9d1-125">Выбранные пользователем сертификаты будут добавлены в это хранилище.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-125">The certificates selected by the user will be added to this store.</span></span><br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <span data-ttu-id="5c9d1-126"><dt>**ДИНАМИЧЕСКОЙ КОМПОНОВКИ CRYPTUI \_ селектцерт \_ Размещение \_ \_ сверху**</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-126"><dt>**CRYPTUI\_SELECTCERT\_PUT\_WINDOW\_TOPMOST**</dt></span></span> </dl> | <span data-ttu-id="5c9d1-127">Заставляет пользовательский интерфейс шифрования быть верхним окном на экране.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-127">Forces the cryptography UI to be the top window on the screen.</span></span><br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="5c9d1-128">**сзтитле**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-128">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-129">Заголовок отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-129">The display title for the dialog box.</span></span> <span data-ttu-id="5c9d1-130">Если значение этого элемента равно **null**, используется заголовок по умолчанию "Select Certificate".</span><span class="sxs-lookup"><span data-stu-id="5c9d1-130">If the value of this member is **NULL**, the default title of "Select Certificate" is used.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-131">**двдонтусеколумн**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-131">**dwDontUseColumn**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-132">Флаги, которые можно комбинировать, чтобы исключить столбцы дисплея.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-132">Flags that can be combined to exclude columns of the display.</span></span>



| <span data-ttu-id="5c9d1-133">Значение</span><span class="sxs-lookup"><span data-stu-id="5c9d1-133">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="5c9d1-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5c9d1-134">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <span data-ttu-id="5c9d1-135"><dt>**Динамической компоновки Cryptui \_ SELECT \_ ISSUEDTO, \_ столбец**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-135"><dt>**CRYPTUI\_SELECT\_ISSUEDTO\_COLUMN**</dt> <dt>1 (0x1)</dt></span></span> </dl>             | <span data-ttu-id="5c9d1-136">Не отображать сведения о **ISSUEDTO** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-136">Do not display **ISSUEDTO** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <span data-ttu-id="5c9d1-137"><dt>**Динамической компоновки Cryptui \_ SELECT \_ ISSUEDBY, \_ столбец**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-137"><dt>**CRYPTUI\_SELECT\_ISSUEDBY\_COLUMN**</dt> <dt>2 (0x2)</dt></span></span> </dl>             | <span data-ttu-id="5c9d1-138">Не отображать сведения о **ISSUEDBY** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-138">Do not display **ISSUEDBY** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <span data-ttu-id="5c9d1-139"><dt>**Динамической компоновки Cryptui \_ SELECT \_ интендедусе, \_ столбец**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-139"><dt>**CRYPTUI\_SELECT\_INTENDEDUSE\_COLUMN**</dt> <dt>4 (0x4)</dt></span></span> </dl>    | <span data-ttu-id="5c9d1-140">Не отображать сведения о **интендедусе** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-140">Do not display **IntendedUse** information.</span></span><br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <span data-ttu-id="5c9d1-141"><dt>**Динамической компоновки Cryptui \_ Выбор \_ FRIENDLYNAME \_ столбца**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-141"><dt>**CRYPTUI\_SELECT\_FRIENDLYNAME\_COLUMN**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="5c9d1-142">Не отображать сведения об имени.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-142">Do not display name information.</span></span><br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <span data-ttu-id="5c9d1-143"><dt>**Динамической компоновки Cryptui \_ Выберите \_ расположение \_ столбец**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-143"><dt>**CRYPTUI\_SELECT\_LOCATION\_COLUMN**</dt> <dt>16 (0x10)</dt></span></span> </dl>           | <span data-ttu-id="5c9d1-144">Не отображать сведения о расположении.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-144">Do not display location information.</span></span><br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <span data-ttu-id="5c9d1-145"><dt>**Динамической компоновки Cryptui \_ Выберите \_ \_ столбец истечения срока действия**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="5c9d1-145"><dt>**CRYPTUI\_SELECT\_EXPIRATION\_COLUMN**</dt> <dt>32 (0x20)</dt></span></span> </dl>     | <span data-ttu-id="5c9d1-146">Не отображать сведения об истечении срока действия.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-146">Do not display expiration information.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="5c9d1-147">**сздисплайстринг**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-147">**szDisplayString**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-148">Текст, отображаемый в диалоговом окне для указания пользователю.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-148">Text that is displayed in the dialog box to instruct the user.</span></span> <span data-ttu-id="5c9d1-149">Если значение этого элемента равно **null**, используется строка по умолчанию "выберите сертификат, который вы хотите использовать".</span><span class="sxs-lookup"><span data-stu-id="5c9d1-149">If the value of this member is **NULL**, the default string "Select a certificate you want to use" is used.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-150">**пфилтеркаллбакк**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-150">**pFilterCallback**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-151">Указатель на функцию обратного вызова [**пфнкфилтерпрок**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) , которая фильтрует сертификаты, отображаемые в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-151">A pointer to a [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) callback function that filters the certificates that are displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-152">**пдисплайкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-152">**pDisplayCallback**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-153">Указатель на функцию обратного вызова [**пфнкцертдисплайпрок**](pfnccertdisplayproc.md) , которая отображает сертификаты, которые пользователь выбирает для просмотра.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-153">A pointer to a [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) callback function that displays certificates that the user selects to view.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-154">**пвкаллбаккдата**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-154">**pvCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-155">Дополнительные данные, передаваемые в функции обратного вызова, указанные членами **пфилтеркаллбакк** и **пдисплайкаллбакк** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-155">Additional data that is passed to the callback functions specified by the **pFilterCallback** and **pDisplayCallback** members.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-156">**кдисплайсторес**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-156">**cDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-157">Количество хранилищ сертификатов в массиве **ргхдисплайсторес** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-157">The number of certificate stores in the **rghDisplayStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-158">**ргхдисплайсторес**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-158">**rghDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-159">Указатель на массив хранилищ, который содержит сертификаты, доступные для выбора в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-159">A pointer to an array of stores that contain certificates available for selection in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-160">**ксторес**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-160">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-161">Количество хранилищ сертификатов в массиве **ргхсторес** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-161">The number of certificate stores in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-162">**ргхсторес**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-162">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-163">Указатель на массив хранилищ сертификатов для поиска при создании цепочки сертификатов и проверки доверия для сертификатов, отображаемых в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-163">A pointer to an array of certificate stores to search when building a certificate chain and verifying trust for the certificates displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-164">**кпропшитпажес**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-164">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-165">Количество страниц свойств в массиве **ргпропшитпажес** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-165">The number of property pages in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-166">**ргпропшитпажес**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-166">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-167">Указатель на массив структур **пропшитпаже** , представляющих страницы свойств, которые передаются в диалоговое окно просмотра сертификата при выборе сертификата для просмотра.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-167">A pointer to an array of **PROPSHEETPAGE** structures that represent property pages that are passed to the certificate viewing dialog box when a certificate is selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="5c9d1-168">**хселектедцертсторе**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-168">**hSelectedCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="5c9d1-169">Маркер хранилища сертификатов, созданный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-169">A handle to a certificate store created by the caller.</span></span> <span data-ttu-id="5c9d1-170">Выбранные пользователем сертификаты будут добавлены в это хранилище.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-170">The certificates selected by the user are added to this store.</span></span> <span data-ttu-id="5c9d1-171">Если число сертификатов в этом хранилище одинаково до и после вызова [**криптуидлгселектцертификате**](cryptuidlgselectcertificate.md), пользователь закрыл диалоговое окно, не выбирая сертификаты.</span><span class="sxs-lookup"><span data-stu-id="5c9d1-171">If the number of certificates in this store is the same before and after calling [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), the user closed the dialog box without selecting any certificates.</span></span>

<span data-ttu-id="5c9d1-172">Этот элемент не используется, если элемент **dwFlags** этой структуры не содержит флаг **динамической компоновки Cryptui \_ селектцерт \_ SELECT** .</span><span class="sxs-lookup"><span data-stu-id="5c9d1-172">This member is not used if the **dwFlags** member of this structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c9d1-173">Требования</span><span class="sxs-lookup"><span data-stu-id="5c9d1-173">Requirements</span></span>



| <span data-ttu-id="5c9d1-174">Требование</span><span class="sxs-lookup"><span data-stu-id="5c9d1-174">Requirement</span></span> | <span data-ttu-id="5c9d1-175">Значение</span><span class="sxs-lookup"><span data-stu-id="5c9d1-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9d1-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c9d1-176">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9d1-177">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5c9d1-177">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="5c9d1-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c9d1-178">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9d1-179">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5c9d1-179">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="5c9d1-180">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="5c9d1-180">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5c9d1-181">**Динамической компоновки Cryptui \_ СЕЛЕКТЦЕРТИФИКАТЕ \_ структв** (Юникод) и **динамической компоновки Cryptui \_ селектцертификате \_ struct** a (ANSI)</span><span class="sxs-lookup"><span data-stu-id="5c9d1-181">**CRYPTUI\_SELECTCERTIFICATE\_STRUCTW** (Unicode) and **CRYPTUI\_SELECTCERTIFICATE\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c9d1-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c9d1-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c9d1-183">**криптуидлгселектцертификате**</span><span class="sxs-lookup"><span data-stu-id="5c9d1-183">**CryptUIDlgSelectCertificate**</span></span>](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




