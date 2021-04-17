---
description: Свойство Куалифиердескриптион только для чтения возвращает текстовую строку, описывающую квалифицированный компонент.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Свойство Installer. Куалифиердескриптион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652163"
---
# <a name="installerqualifierdescription-property"></a>Свойство Installer. Куалифиердескриптион

Свойство **куалифиердескриптион** только для чтения возвращает текстовую строку, описывающую квалифицированный компонент. Эта локализуемое строка создается в столбце AppData [таблицы публишкомпонент](publishcomponent-table.md) и может отображаться для пользователя. Квалификатор различает несколько форм одного компонента, например компонент, реализованный на нескольких языках.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a>Значение свойства

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. установщик Windows в Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Компоненты с квалификаторами](qualified-components.md)
</dt> </dl>

 

 




