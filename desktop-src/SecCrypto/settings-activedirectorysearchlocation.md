---
description: Задает или получает расположение поиска Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Свойство Settings. Активедиректорисеарчлокатион
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
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668764"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Свойство Settings. Активедиректорисеарчлокатион

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

[**Параметры**](settings.md)
</dt> </dl>

 

 




