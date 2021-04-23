---
description: Локальный администратор безопасности (LSA) предоставляет функции для преобразования имен пользователей, групп и локальных групп, а также соответствующих значений идентификаторов безопасности (SID).
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Преобразование между именами и идентификаторами безопасности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682575"
---
# <a name="translating-between-names-and-sids"></a><span data-ttu-id="7a34e-103">Преобразование между именами и идентификаторами безопасности</span><span class="sxs-lookup"><span data-stu-id="7a34e-103">Translating Between Names and SIDs</span></span>

<span data-ttu-id="7a34e-104">[*Локальный администратор безопасности*](/windows/desktop/SecGloss/l-gly) (LSA) предоставляет функции для преобразования имен пользователей, групп и локальных групп, а также соответствующих значений [*идентификаторов безопасности*](/windows/desktop/SecGloss/s-gly) (SID).</span><span class="sxs-lookup"><span data-stu-id="7a34e-104">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) provides functions to translate between user, group, and local group names and their corresponding [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) values.</span></span> <span data-ttu-id="7a34e-105">Чтобы указать имена учетных записей, вызовите функцию [**лсалукупнамес**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) .</span><span class="sxs-lookup"><span data-stu-id="7a34e-105">To locate account names, call the [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) function.</span></span> <span data-ttu-id="7a34e-106">Эта функция возвращает идентификатор безопасности в виде пары RID или индекса домена.</span><span class="sxs-lookup"><span data-stu-id="7a34e-106">This function returns the SID as a RID/Domain index pair.</span></span> <span data-ttu-id="7a34e-107">Чтобы получить идентификатор безопасности в виде одного элемента, вызовите функцию [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) .</span><span class="sxs-lookup"><span data-stu-id="7a34e-107">To get the SID as a single element, call the [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) function.</span></span> <span data-ttu-id="7a34e-108">Чтобы узнать идентификаторы SID, вызовите [**лсалукупсидс**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span><span class="sxs-lookup"><span data-stu-id="7a34e-108">To locate SIDs, call [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span></span>

<span data-ttu-id="7a34e-109">Эти функции могут преобразовывать сведения о имени и идентификаторе безопасности из любого домена, которому доверяет локальная система.</span><span class="sxs-lookup"><span data-stu-id="7a34e-109">These functions can translate name and SID information from any domain trusted by the local system.</span></span>

<span data-ttu-id="7a34e-110">Прежде чем можно будет выполнить преобразование между именами учетных записей и идентификаторами безопасности, приложение должно получить обработчик для объекта локальной [**политики**](policy-object.md) , как показано при [открытии обработчика объектов политики](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="7a34e-110">Before you can translate between account names and SIDs, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="7a34e-111">В следующем примере выполняется поиск идентификатора безопасности для учетной записи с учетом ее имени.</span><span class="sxs-lookup"><span data-stu-id="7a34e-111">The following example looks up the SID for an account, given the account name.</span></span>


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



<span data-ttu-id="7a34e-112">В предыдущем примере функция **инитлсастринг** преобразует строку Юникода в структуру [**\_ \_ строки Юникода LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="7a34e-112">In the preceding example, the function **InitLsaString** converts a Unicode string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="7a34e-113">Код для этой функции показан в [использовании строк Юникода в формате LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="7a34e-113">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

> [!Note]  
> <span data-ttu-id="7a34e-114">Эти функции перевода в основном предоставляются для использования редакторами разрешений для вывода сведений [*списка управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="7a34e-114">These translation functions are primarily provided for use by permissions editors to display [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) information.</span></span> <span data-ttu-id="7a34e-115">Редактор разрешений всегда должен вызывать эти функции с помощью объекта [**политики**](policy-object.md) для системы, в которой находятся имя или [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) SID.</span><span class="sxs-lookup"><span data-stu-id="7a34e-115">A permission editor should always call these functions using the [**Policy**](policy-object.md) object for the system where the name or [*security identifier*](/windows/desktop/SecGloss/s-gly) SID is located.</span></span> <span data-ttu-id="7a34e-116">Это гарантирует, что во время перевода будет создана ссылка на соответствующий набор доверенных доменов.</span><span class="sxs-lookup"><span data-stu-id="7a34e-116">This ensures that the proper set of trusted domains is referenced during the translation.</span></span>

 

<span data-ttu-id="7a34e-117">Система управления доступом Windows также предоставляет функции, выполняющие переводы между идентификаторами безопасности и именами учетных записей: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) и [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span><span class="sxs-lookup"><span data-stu-id="7a34e-117">Windows Access Control also provides functions that perform translations between SIDs and account names: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) and [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="7a34e-118">Если приложению требуется найти имя учетной записи или идентификатор безопасности и не использовать дополнительные функции политики LSA, используйте функции управления доступом Windows, а не функции политики LSA.</span><span class="sxs-lookup"><span data-stu-id="7a34e-118">If your application needs to look up an account name or SID and does not use additional LSA Policy functionality, use the Windows Access Control functions instead of the LSA Policy functions.</span></span> <span data-ttu-id="7a34e-119">Дополнительные сведения об этих функциях см. в разделе [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="7a34e-119">For more information about these functions, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

 

 
