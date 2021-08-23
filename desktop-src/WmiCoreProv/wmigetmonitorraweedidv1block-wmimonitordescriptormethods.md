---
description: Получает необработанные данные для указанной расширенной структуры (E-EDID), которая определяет оптимальные параметры для настройки монитора.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Метод WmiGetMonitorRawEEdidV1Block класса Вмимонитордескриптормесодс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: dacd0c44a6c0fa8270a65155583f8041616f98674d0798db8b13a72d13751653
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558089"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>Метод WmiGetMonitorRawEEdidV1Block класса Вмимонитордескриптормесодс

Метод **WmiGetMonitorRawEEdidV1Block** получает необработанные данные для указанной расширенной структуры (E-EDID), которая определяет оптимальные параметры для настройки монитора.

## <a name="syntax"></a>Синтаксис


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ИД блока* \[ окне\]
</dt> <dd>

Удостоверение блока данных.

</dd> <dt>

*Блокктипе* \[ заполняет\]
</dt> <dd>

Тип блока данных. В следующей таблице перечислены возможные возвращаемые значения.



| Значение                                                                                 | Значение                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Не инициализировано<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Базовый блок EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Блочная схема EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Другие<br/>           |



 

</dd> <dt>

*Блоккконтент* \[ заполняет\]
</dt> <dd>

128-байтовый массив, содержащий необработанное содержимое блока.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает ноль (0), чтобы указать на успешное выполнение. Любое другое значение указывает на ошибку. Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Примеры

Следующий пример кода извлекает блоки EDID любого дисплея как необработанные 128 битовых массивов.


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Пространство имен<br/>                | Корневой \\ инструментарий WMI<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Вмикоре. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**вмимонитордескриптормесодс**](wmimonitordescriptormethods.md)
</dt> <dt>

[**мсмониторкласс**](msmonitorclass.md)
</dt> </dl>

 

