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
ms.openlocfilehash: bfa316b4ff01f6e5667b3fb2c5fce2333c4b4aaf34dc5a1dbb37feb61d1a9ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894034"
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

Строка, содержащая разделенный точками с запятой список исправлений для удаления. Каждое исправление может быть представлено полным путем к пакету исправлений или идентификатором GUID исправления. Это обязательный параметр.

</dd> <dt>

*ProductCode* 
</dt> <dd>

Строка с идентификатором GUID продукта, из которого удаляются исправления. Это обязательный параметр.

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

## <a name="remarks"></a>Remarks

Пример, демонстрирующий, как приложение может удалить исправление из всех доступных для пользователя продуктов, см. в разделе Удаление [исправлений](uninstalling-patches.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Windows установщик 5,0 на Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7. Windows установщик 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista. Windows установщик 3,0 или более поздней версии на Windows Server 2003 или Windows XP.<br/> |
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

[не поддерживается в установщик Windows 2,0 и более ранних версиях](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




