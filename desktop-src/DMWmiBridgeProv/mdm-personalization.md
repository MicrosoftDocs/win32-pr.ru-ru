---
title: Класс MDM_Personalization
description: '\_Класс персонализации MDM используется для задания экрана блокировки и фоновых изображений рабочего стола. Установка этих политик также не позволяет пользователю изменять образ.'
ms.assetid: 99b60767-b321-4ec6-9802-76221d26c830
keywords:
- Класс MDM_Personalization
- MDM_Personalization класс, описание
topic_type:
- apiref
api_name:
- MDM_Personalization
- MDM_Personalization.InstanceID
- MDM_Personalization.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0039021d8c05599f91513344d4cbee010944e0944f08f0b258294d91e9714f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967514"
---
# <a name="mdm_personalization-class"></a>\_Класс персонализации MDM

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

\_Класс персонализации MDM используется для задания экрана блокировки и фоновых изображений рабочего стола. Установка этих политик также не позволяет пользователю изменять образ.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Personalization
{
  string InstanceID;
  string ParentID;
  string DesktopImageUrl;
  sint32 DesktopImageStatus;
  string LockScreenImageUrl;
  sint32 LockScreenImageStatus;
};
```

## <a name="members"></a>Члены

Класс **\_ персонализации MDM** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ персонализации MDM** имеет следующие свойства.

<dl> <dt>

[десктопимажестатус](/windows/client-management/mdm/personalization-csp#desktopimagestatus)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[DesktopImageUrl](/windows/client-management/mdm/personalization-csp#desktopimageurl)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[локкскринимажестатус](/windows/client-management/mdm/personalization-csp#lockscreenimagestatus)
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

[LockScreenImageUrl](/windows/client-management/mdm/personalization-csp#lockscreenimageurl)
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                     |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

