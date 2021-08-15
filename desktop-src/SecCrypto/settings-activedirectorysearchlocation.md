---
description: Задает или получает расположение поиска Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Параметры. Активедиректорисеарчлокатион, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 884866fd5ff6a3e3ff483a255bf2b77063ca81e51141108c9f58fd45629cc036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900324"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Параметры. Активедиректорисеарчлокатион, свойство

\[Свойство **активедиректорисеарчлокатион** доступно для использования в операционных системах, указанных в разделе требования.\]

Свойство **активедиректорисеарчлокатион** задает или получает расположение поиска Active Directory.

## <a name="syntax"></a>Синтаксис


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Значение свойства

Значение перечисления [**CAPICOM \_ Active \_ Directory \_ \_**](capicom-active-directory-search-location.md) , указывающее место поиска. По умолчанию используется значение CAPICOM \_ Search \_ ANY. В следующей таблице приводятся возможные значения.



| Значение                                                                                                                                                                                                           | Значение                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**CAPICOM \_ Поиск \_**</dt> </dl>                                   | Поиск по всем доступным расположениям.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**\_Поиск в \_ домене CAPICOM по умолчанию \_**</dt> </dl> | Поиск только по домену по умолчанию.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CAPICOM \_ Поиск в \_ глобальном \_ каталоге**</dt> </dl> | Поиск только в глобальном каталоге.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**"Настройки"**](settings.md)
</dt> </dl>

 

 




