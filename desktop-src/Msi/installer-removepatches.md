---
description: Метод Ремовепатчес удаляет один или несколько исправлений для продуктов, которые могут получить исправление. Метод Ремовепатчес вызывает Мсиремовепатчес.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Метод Installer. Ремовепатчес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651980"
---
# <a name="installerremovepatches-method"></a>Метод Installer. Ремовепатчес

Метод **ремовепатчес** удаляет один или несколько исправлений для продуктов, которые могут получить исправление. Метод **ремовепатчес** вызывает [**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).

## <a name="syntax"></a>Синтаксис


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*патчлист* 
</dt> <dd>

Строка, содержащая разделенный точками с запятой список исправлений для удаления. Каждое исправление может быть представлено полным путем к пакету исправлений или идентификатором GUID исправления. Этот параметр обязателен.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Строка с идентификатором GUID продукта, из которого удаляются исправления. Этот параметр обязателен.

</dd> <dt>

*унинсталлтипе* 
</dt> <dd>

Целочисленное значение, указывающее тип удаления исправления. Этот параметр должен быть **мсиинсталлтипесинглеинстанце**.

</dd> <dt>

*PropertyList* 
</dt> <dd>

Строка, указывающая пары "свойство = значение" для включения. Этот параметр является необязательным.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Пример, демонстрирующий, как приложение может удалить исправление из всех доступных для пользователя продуктов, см. в разделе Удаление [исправлений](uninstalling-patches.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Установщик Windows 3,0 или более поздней версии в Windows Server 2003 или Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ProductCode**](productcode.md)
</dt> <dt>

[**мсиремовепатчес**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Удаление исправлений](uninstalling-patches.md)
</dt> <dt>

[Не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




