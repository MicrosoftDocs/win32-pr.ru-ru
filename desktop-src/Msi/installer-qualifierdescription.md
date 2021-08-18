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
ms.openlocfilehash: c226f00d7f95b4585fa4a0713fb281011079cdc35c4e421254beec75db84d7db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763584"
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
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик на Windows Server 2003 или Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**мсиенумкомпоненткуалифиерс**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[Компоненты с квалификаторами](qualified-components.md)
</dt> </dl>

 

 




