<?xml version="1.0" encoding="UTF-8"?>
<bpmn:definitions xmlns:bpmn="http://www.omg.org/spec/BPMN/20100524/MODEL" xmlns:bpmndi="http://www.omg.org/spec/BPMN/20100524/DI" xmlns:dc="http://www.omg.org/spec/DD/20100524/DC" xmlns:di="http://www.omg.org/spec/DD/20100524/DI" id="Definitions_0ddkqgr" targetNamespace="http://bpmn.io/schema/bpmn" exporter="Camunda Modeler" exporterVersion="3.0.0-dev">
  <bpmn:collaboration id="Collaboration_06ftemy">
    <bpmn:participant id="Participant_0nu1w1b" name="🔥Мой процесс (нажмите 2 раза на эту строку, чтобы переименовать)" processRef="Process_1d4oa6g46" />
    <bpmn:textAnnotation id="TextAnnotation_0cmctii">
      <bpmn:text>Клиент указывает: тип авто, дату и время, адрес, бокс</bpmn:text>
    </bpmn:textAnnotation>
    <bpmn:association id="Association_14gerv3" associationDirection="None" sourceRef="Activity_1tmjtvv" targetRef="TextAnnotation_0cmctii" />
  </bpmn:collaboration>
  <bpmn:process id="Process_1d4oa6g46" isExecutable="false">
    <bpmn:laneSet id="LaneSet_016uj8o">
      <bpmn:lane id="Lane_1er8dgc" name="Кдиент">
        <bpmn:flowNodeRef>StartEvent_1</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1tmjtvv</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_03pjtbv</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_14r0mcb</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0fbfg3f</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_0vjc0x5</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1gm3pz6</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_0nvs3g2</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_03fgt7d</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1fqvkhs</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1ca1cpe</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1x7vb7m</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1kil3ck</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_1axlw13</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Event_1bjrpa8</bpmn:flowNodeRef>
      </bpmn:lane>
      <bpmn:lane id="Lane_0xq8vkf" name="Си стема">
        <bpmn:flowNodeRef>Activity_01hfkmi</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0q9m1gi</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0qm4ila</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_0a2g60z</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_1joywdw</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0cpgbhb</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_138s1xb</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_1rvsps2</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Gateway_1k64xx3</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_10fsepm</bpmn:flowNodeRef>
      </bpmn:lane>
      <bpmn:lane id="Lane_1quauyo" name="Платежный шлюз">
        <bpmn:flowNodeRef>Activity_1hpemsb</bpmn:flowNodeRef>
        <bpmn:flowNodeRef>Activity_0uk5yut</bpmn:flowNodeRef>
      </bpmn:lane>
    </bpmn:laneSet>
    <bpmn:sequenceFlow id="Flow_1vah68s" sourceRef="Activity_0uk5yut" targetRef="Activity_1joywdw" />
    <bpmn:sequenceFlow id="Flow_1qyixhp" name="ДА" sourceRef="Gateway_0a2g60z" targetRef="Activity_0uk5yut" />
    <bpmn:sequenceFlow id="Flow_0f3ibj7" sourceRef="Activity_0qm4ila" targetRef="Gateway_0a2g60z" />
    <bpmn:sequenceFlow id="Flow_09in172" sourceRef="Activity_1x7vb7m" targetRef="Activity_0qm4ila" />
    <bpmn:sequenceFlow id="Flow_1pmu88m" sourceRef="Activity_1ca1cpe" targetRef="Event_1bjrpa8" />
    <bpmn:sequenceFlow id="Flow_1jreq8y" name="НЕТ" sourceRef="Gateway_03fgt7d" targetRef="Activity_1ca1cpe" />
    <bpmn:sequenceFlow id="Flow_14ecn7x" name="ДА" sourceRef="Gateway_03fgt7d" targetRef="Activity_1x7vb7m" />
    <bpmn:sequenceFlow id="Flow_1v9xf5m" sourceRef="Activity_1fqvkhs" targetRef="Gateway_03fgt7d" />
    <bpmn:sequenceFlow id="Flow_0exlgea" name="ДА" sourceRef="Gateway_1k64xx3" targetRef="Activity_1kil3ck" />
    <bpmn:sequenceFlow id="Flow_1xq5595" sourceRef="Activity_1hpemsb" targetRef="Activity_0cpgbhb" />
    <bpmn:sequenceFlow id="Flow_07onu86" name="ДА" sourceRef="Gateway_0nvs3g2" targetRef="Activity_1hpemsb" />
    <bpmn:sequenceFlow id="Flow_1srqp7f" name="НЕТ" sourceRef="Gateway_0nvs3g2" targetRef="Gateway_03fgt7d" />
    <bpmn:sequenceFlow id="Flow_006195u" sourceRef="Activity_1joywdw" targetRef="Gateway_0nvs3g2" />
    <bpmn:sequenceFlow id="Flow_06xq0z6" sourceRef="Activity_1gm3pz6" targetRef="Activity_0qm4ila" />
    <bpmn:sequenceFlow id="Flow_1lsep1w" name="НЕТ" sourceRef="Gateway_0a2g60z" targetRef="Activity_1gm3pz6" />
    <bpmn:sequenceFlow id="Flow_19wix61" sourceRef="Activity_0fbfg3f" targetRef="Gateway_0vjc0x5" />
    <bpmn:sequenceFlow id="Flow_03kt94x" name="НЕТ" sourceRef="Gateway_1rvsps2" targetRef="Activity_0fbfg3f" />
    <bpmn:sequenceFlow id="Flow_0amnj94" name="ДА" sourceRef="Gateway_14r0mcb" targetRef="Activity_1fqvkhs" />
    <bpmn:sequenceFlow id="Flow_1r06ujv" sourceRef="Activity_03pjtbv" targetRef="Gateway_14r0mcb" />
    <bpmn:sequenceFlow id="Flow_1x8x4em" sourceRef="Activity_0q9m1gi" targetRef="Gateway_1rvsps2" />
    <bpmn:sequenceFlow id="Flow_1vc0d99" name="ДА" sourceRef="Gateway_0vjc0x5" targetRef="Activity_0q9m1gi" />
    <bpmn:sequenceFlow id="Flow_1hmiwsl" sourceRef="Activity_01hfkmi" targetRef="Activity_03pjtbv" />
    <bpmn:sequenceFlow id="Flow_1g7v2ai" name="ДА" sourceRef="Gateway_1rvsps2" targetRef="Activity_01hfkmi" />
    <bpmn:sequenceFlow id="Flow_1t0ejbc" sourceRef="Activity_10fsepm" targetRef="Activity_0q9m1gi" />
    <bpmn:sequenceFlow id="Flow_1992bdp" sourceRef="Activity_1tmjtvv" targetRef="Activity_10fsepm" />
    <bpmn:sequenceFlow id="Flow_01vvoai" name="НЕТ" sourceRef="Gateway_0vjc0x5" targetRef="Activity_1tmjtvv" />
    <bpmn:sequenceFlow id="Flow_05z3apo" name="НЕТ" sourceRef="Gateway_14r0mcb" targetRef="Activity_1tmjtvv" />
    <bpmn:sequenceFlow id="Flow_0lqoezz" name="Клиент открыл приложение" sourceRef="StartEvent_1" targetRef="Activity_1tmjtvv" />
    <bpmn:task id="Activity_1joywdw" name="Подтверждение  о списании">
      <bpmn:incoming>Flow_1vah68s</bpmn:incoming>
      <bpmn:outgoing>Flow_006195u</bpmn:outgoing>
    </bpmn:task>
    <bpmn:task id="Activity_0uk5yut" name="Запрос на списание">
      <bpmn:incoming>Flow_1qyixhp</bpmn:incoming>
      <bpmn:outgoing>Flow_1vah68s</bpmn:outgoing>
    </bpmn:task>
    <bpmn:exclusiveGateway id="Gateway_0a2g60z" name="Карта введена корректно?">
      <bpmn:incoming>Flow_0f3ibj7</bpmn:incoming>
      <bpmn:outgoing>Flow_1lsep1w</bpmn:outgoing>
      <bpmn:outgoing>Flow_1qyixhp</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:serviceTask id="Activity_0qm4ila" name="Проверить реквизиты карты">
      <bpmn:incoming>Flow_09in172</bpmn:incoming>
      <bpmn:incoming>Flow_06xq0z6</bpmn:incoming>
      <bpmn:outgoing>Flow_0f3ibj7</bpmn:outgoing>
    </bpmn:serviceTask>
    <bpmn:task id="Activity_1hpemsb" name="Оплата">
      <bpmn:incoming>Flow_07onu86</bpmn:incoming>
      <bpmn:outgoing>Flow_1xq5595</bpmn:outgoing>
    </bpmn:task>
    <bpmn:userTask id="Activity_1x7vb7m" name="Оплатить картой в приложении">
      <bpmn:incoming>Flow_14ecn7x</bpmn:incoming>
      <bpmn:outgoing>Flow_09in172</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:task id="Activity_1ca1cpe" name="Оплатить на месте">
      <bpmn:incoming>Flow_1jreq8y</bpmn:incoming>
      <bpmn:outgoing>Flow_1pmu88m</bpmn:outgoing>
    </bpmn:task>
    <bpmn:task id="Activity_1fqvkhs" name="Выбор способа оплаты">
      <bpmn:incoming>Flow_0amnj94</bpmn:incoming>
      <bpmn:outgoing>Flow_1v9xf5m</bpmn:outgoing>
    </bpmn:task>
    <bpmn:exclusiveGateway id="Gateway_03fgt7d" name="Онлайн оплата?">
      <bpmn:incoming>Flow_1srqp7f</bpmn:incoming>
      <bpmn:incoming>Flow_1v9xf5m</bpmn:incoming>
      <bpmn:outgoing>Flow_14ecn7x</bpmn:outgoing>
      <bpmn:outgoing>Flow_1jreq8y</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:exclusiveGateway id="Gateway_0nvs3g2" name="Подтверждаю?">
      <bpmn:incoming>Flow_006195u</bpmn:incoming>
      <bpmn:outgoing>Flow_07onu86</bpmn:outgoing>
      <bpmn:outgoing>Flow_1srqp7f</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:userTask id="Activity_1gm3pz6" name="Ввести реквизиты карты">
      <bpmn:incoming>Flow_1lsep1w</bpmn:incoming>
      <bpmn:outgoing>Flow_06xq0z6</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:exclusiveGateway id="Gateway_0vjc0x5">
      <bpmn:incoming>Flow_19wix61</bpmn:incoming>
      <bpmn:outgoing>Flow_1vc0d99</bpmn:outgoing>
      <bpmn:outgoing>Flow_01vvoai</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:userTask id="Activity_0fbfg3f" name="Бокс занят.  Выбрать другой слот">
      <bpmn:incoming>Flow_03kt94x</bpmn:incoming>
      <bpmn:outgoing>Flow_19wix61</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:exclusiveGateway id="Gateway_1rvsps2" name="Бокс доступен?">
      <bpmn:incoming>Flow_1x8x4em</bpmn:incoming>
      <bpmn:outgoing>Flow_1g7v2ai</bpmn:outgoing>
      <bpmn:outgoing>Flow_03kt94x</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:exclusiveGateway id="Gateway_14r0mcb" name="Адрес и бокс выбраны верно?">
      <bpmn:incoming>Flow_1r06ujv</bpmn:incoming>
      <bpmn:outgoing>Flow_0amnj94</bpmn:outgoing>
      <bpmn:outgoing>Flow_05z3apo</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:userTask id="Activity_03pjtbv" name="Подтвердить выбор мойки и перейти к оплате">
      <bpmn:incoming>Flow_1hmiwsl</bpmn:incoming>
      <bpmn:outgoing>Flow_1r06ujv</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:serviceTask id="Activity_0q9m1gi" name="Проверить наличие свободного бокса">
      <bpmn:incoming>Flow_1vc0d99</bpmn:incoming>
      <bpmn:incoming>Flow_1t0ejbc</bpmn:incoming>
      <bpmn:outgoing>Flow_1x8x4em</bpmn:outgoing>
    </bpmn:serviceTask>
    <bpmn:serviceTask id="Activity_01hfkmi" name="Заблокировать слот на N минут">
      <bpmn:incoming>Flow_1g7v2ai</bpmn:incoming>
      <bpmn:outgoing>Flow_1hmiwsl</bpmn:outgoing>
    </bpmn:serviceTask>
    <bpmn:userTask id="Activity_1tmjtvv" name="Выбор параметров услуги">
      <bpmn:incoming>Flow_0lqoezz</bpmn:incoming>
      <bpmn:incoming>Flow_05z3apo</bpmn:incoming>
      <bpmn:incoming>Flow_01vvoai</bpmn:incoming>
      <bpmn:outgoing>Flow_1992bdp</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:startEvent id="StartEvent_1" name="Клиент">
      <bpmn:outgoing>Flow_0lqoezz</bpmn:outgoing>
    </bpmn:startEvent>
    <bpmn:sequenceFlow id="Flow_1vqtafe" sourceRef="Activity_0cpgbhb" targetRef="Activity_138s1xb" />
    <bpmn:task id="Activity_0cpgbhb" name="Оплата прошла успешно">
      <bpmn:incoming>Flow_1xq5595</bpmn:incoming>
      <bpmn:outgoing>Flow_1vqtafe</bpmn:outgoing>
    </bpmn:task>
    <bpmn:task id="Activity_138s1xb" name="Создание напоминания о записи">
      <bpmn:incoming>Flow_1vqtafe</bpmn:incoming>
      <bpmn:outgoing>Flow_0icw5c7</bpmn:outgoing>
    </bpmn:task>
    <bpmn:exclusiveGateway id="Gateway_1k64xx3">
      <bpmn:incoming>Flow_0icw5c7</bpmn:incoming>
      <bpmn:outgoing>Flow_1ru6ws5</bpmn:outgoing>
      <bpmn:outgoing>Flow_0exlgea</bpmn:outgoing>
    </bpmn:exclusiveGateway>
    <bpmn:sequenceFlow id="Flow_0icw5c7" sourceRef="Activity_138s1xb" targetRef="Gateway_1k64xx3" />
    <bpmn:sequenceFlow id="Flow_1ru6ws5" name="НЕТ" sourceRef="Gateway_1k64xx3" targetRef="Event_1axlw13" />
    <bpmn:userTask id="Activity_1kil3ck" name="Push-уведомление о записи за N период времени">
      <bpmn:incoming>Flow_0exlgea</bpmn:incoming>
      <bpmn:outgoing>Flow_16gnlzt</bpmn:outgoing>
    </bpmn:userTask>
    <bpmn:endEvent id="Event_1axlw13" name="Заказ оплачен и подтвержден">
      <bpmn:incoming>Flow_1ru6ws5</bpmn:incoming>
      <bpmn:incoming>Flow_16gnlzt</bpmn:incoming>
      <bpmn:messageEventDefinition id="MessageEventDefinition_0aehrhr" />
    </bpmn:endEvent>
    <bpmn:sequenceFlow id="Flow_16gnlzt" sourceRef="Activity_1kil3ck" targetRef="Event_1axlw13" />
    <bpmn:endEvent id="Event_1bjrpa8" name="Заказ подтвержден но не оплачен">
      <bpmn:incoming>Flow_1pmu88m</bpmn:incoming>
      <bpmn:messageEventDefinition id="MessageEventDefinition_1jf37sc" />
    </bpmn:endEvent>
    <bpmn:serviceTask id="Activity_10fsepm" name="Поиск доступной мойки по критериям">
      <bpmn:incoming>Flow_1992bdp</bpmn:incoming>
      <bpmn:outgoing>Flow_1t0ejbc</bpmn:outgoing>
    </bpmn:serviceTask>
  </bpmn:process>
  <bpmndi:BPMNDiagram id="BPMNDiagram_1">
    <bpmndi:BPMNPlane id="BPMNPlane_1" bpmnElement="Collaboration_06ftemy">
      <bpmndi:BPMNShape id="Participant_0nu1w1b_di" bpmnElement="Participant_0nu1w1b" isHorizontal="true">
        <dc:Bounds x="-90" y="-150" width="3230" height="910" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Lane_1quauyo_di" bpmnElement="Lane_1quauyo" isHorizontal="true">
        <dc:Bounds x="-60" y="550" width="3200" height="210" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Lane_0xq8vkf_di" bpmnElement="Lane_0xq8vkf" isHorizontal="true">
        <dc:Bounds x="-60" y="280" width="3200" height="270" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Lane_1er8dgc_di" bpmnElement="Lane_1er8dgc" isHorizontal="true">
        <dc:Bounds x="-60" y="-150" width="3200" height="430" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1joywdw_di" bpmnElement="Activity_1joywdw">
        <dc:Bounds x="2070" y="376" width="110" height="90" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0uk5yut_di" bpmnElement="Activity_0uk5yut">
        <dc:Bounds x="1895" y="614" width="100" height="90" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0a2g60z_di" bpmnElement="Gateway_0a2g60z" isMarkerVisible="true">
        <dc:Bounds x="1825" y="396" width="50" height="50" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1813" y="357" width="75" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1gh8qtb_di" bpmnElement="Activity_0qm4ila">
        <dc:Bounds x="1655" y="381" width="115" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1txtqlz_di" bpmnElement="Activity_1hpemsb">
        <dc:Bounds x="2315" y="620" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0h9cj60_di" bpmnElement="Activity_1x7vb7m">
        <dc:Bounds x="1482" y="60" width="110" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1ca1cpe_di" bpmnElement="Activity_1ca1cpe">
        <dc:Bounds x="1482" y="-60" width="110" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1fqvkhs_di" bpmnElement="Activity_1fqvkhs">
        <dc:Bounds x="1120" y="-60" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_03fgt7d_di" bpmnElement="Gateway_03fgt7d" isMarkerVisible="true">
        <dc:Bounds x="1346" y="-45" width="50" height="50" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1260" y="-52" width="84" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0nvs3g2_di" bpmnElement="Gateway_0nvs3g2" isMarkerVisible="true">
        <dc:Bounds x="2230" y="75" width="50" height="50" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2290" y="93" width="78" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1r8wsl4_di" bpmnElement="Activity_1gm3pz6">
        <dc:Bounds x="1895" y="60" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_0vjc0x5_di" bpmnElement="Gateway_0vjc0x5" isMarkerVisible="true">
        <dc:Bounds x="525" y="135" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0jk9btm_di" bpmnElement="Activity_0fbfg3f">
        <dc:Bounds x="620" y="120" width="120" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_1rvsps2_di" bpmnElement="Gateway_1rvsps2" isMarkerVisible="true">
        <dc:Bounds x="655" y="455" width="50" height="50" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="640" y="512" width="80" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_14r0mcb_di" bpmnElement="Gateway_14r0mcb" isMarkerVisible="true">
        <dc:Bounds x="1037" y="140" width="50" height="50" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1117" y="155" width="86" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0npnm1r_di" bpmnElement="Activity_03pjtbv">
        <dc:Bounds x="882" y="115" width="125" height="90" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="BPMNShape_1hcn3wp" bpmnElement="Activity_0q9m1gi">
        <dc:Bounds x="420" y="440" width="120" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="BPMNShape_0y68spw" bpmnElement="Activity_01hfkmi">
        <dc:Bounds x="755" y="340" width="110" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0azrf7u_di" bpmnElement="Activity_10fsepm">
        <dc:Bounds x="230" y="440" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_1pszayq_di" bpmnElement="Activity_1tmjtvv">
        <dc:Bounds x="150" y="-60" width="100" height="80" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="_BPMNShape_StartEvent_2" bpmnElement="StartEvent_1">
        <dc:Bounds x="-28" y="-38" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="-26" y="5" width="38" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_0cpgbhb_di" bpmnElement="Activity_0cpgbhb">
        <dc:Bounds x="2416" y="381" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_138s1xb_di" bpmnElement="Activity_138s1xb">
        <dc:Bounds x="2600" y="381" width="100" height="80" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Gateway_1k64xx3_di" bpmnElement="Gateway_1k64xx3" isMarkerVisible="true">
        <dc:Bounds x="2755" y="396" width="50" height="50" />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Activity_051e9ad_di" bpmnElement="Activity_1kil3ck">
        <dc:Bounds x="2695" y="60" width="170" height="90" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_0uwtaet_di" bpmnElement="Event_1axlw13">
        <dc:Bounds x="2962" y="82" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="3018" y="86" width="84" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNShape id="Event_01f24d4_di" bpmnElement="Event_1bjrpa8">
        <dc:Bounds x="1672" y="-38" width="36" height="36" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1649" y="20" width="83" height="40" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Flow_1vah68s_di" bpmnElement="Flow_1vah68s">
        <di:waypoint x="1995" y="659" />
        <di:waypoint x="2038" y="659" />
        <di:waypoint x="2038" y="421" />
        <di:waypoint x="2070" y="421" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1qyixhp_di" bpmnElement="Flow_1qyixhp">
        <di:waypoint x="1850" y="446" />
        <di:waypoint x="1850" y="654" />
        <di:waypoint x="1895" y="654" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1862" y="462" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0f3ibj7_di" bpmnElement="Flow_0f3ibj7">
        <di:waypoint x="1770" y="421" />
        <di:waypoint x="1825" y="421" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_09in172_di" bpmnElement="Flow_09in172">
        <di:waypoint x="1592" y="100" />
        <di:waypoint x="1635" y="100" />
        <di:waypoint x="1635" y="421" />
        <di:waypoint x="1655" y="421" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1pmu88m_di" bpmnElement="Flow_1pmu88m">
        <di:waypoint x="1592" y="-20" />
        <di:waypoint x="1672" y="-20" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1jreq8y_di" bpmnElement="Flow_1jreq8y">
        <di:waypoint x="1396" y="-20" />
        <di:waypoint x="1482" y="-20" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1420" y="-43" width="23" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_14ecn7x_di" bpmnElement="Flow_14ecn7x">
        <di:waypoint x="1371" y="5" />
        <di:waypoint x="1371" y="100" />
        <di:waypoint x="1482" y="100" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1382" y="43" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1v9xf5m_di" bpmnElement="Flow_1v9xf5m">
        <di:waypoint x="1220" y="-20" />
        <di:waypoint x="1346" y="-20" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0exlgea_di" bpmnElement="Flow_0exlgea">
        <di:waypoint x="2780" y="396" />
        <di:waypoint x="2780" y="150" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2792" y="364" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1xq5595_di" bpmnElement="Flow_1xq5595">
        <di:waypoint x="2415" y="660" />
        <di:waypoint x="2466" y="660" />
        <di:waypoint x="2466" y="461" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_07onu86_di" bpmnElement="Flow_07onu86">
        <di:waypoint x="2255" y="125" />
        <di:waypoint x="2255" y="660" />
        <di:waypoint x="2315" y="660" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2269" y="147" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1srqp7f_di" bpmnElement="Flow_1srqp7f">
        <di:waypoint x="2255" y="75" />
        <di:waypoint x="2255" y="-90" />
        <di:waypoint x="1371" y="-90" />
        <di:waypoint x="1371" y="-45" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2269" y="38" width="23" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_006195u_di" bpmnElement="Flow_006195u">
        <di:waypoint x="2180" y="421" />
        <di:waypoint x="2205" y="421" />
        <di:waypoint x="2205" y="100" />
        <di:waypoint x="2230" y="100" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_06xq0z6_di" bpmnElement="Flow_06xq0z6">
        <di:waypoint x="1895" y="100" />
        <di:waypoint x="1705" y="100" />
        <di:waypoint x="1705" y="381" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1lsep1w_di" bpmnElement="Flow_1lsep1w">
        <di:waypoint x="1875" y="421" />
        <di:waypoint x="1945" y="421" />
        <di:waypoint x="1945" y="140" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1893" y="398" width="23" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_19wix61_di" bpmnElement="Flow_19wix61">
        <di:waypoint x="620" y="160" />
        <di:waypoint x="575" y="160" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_03kt94x_di" bpmnElement="Flow_03kt94x">
        <di:waypoint x="680" y="455" />
        <di:waypoint x="680" y="200" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="692" y="423" width="23" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0amnj94_di" bpmnElement="Flow_0amnj94">
        <di:waypoint x="1062" y="140" />
        <di:waypoint x="1062" y="-20" />
        <di:waypoint x="1120" y="-20" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1082" y="125" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1r06ujv_di" bpmnElement="Flow_1r06ujv">
        <di:waypoint x="1007" y="165" />
        <di:waypoint x="1037" y="165" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1x8x4em_di" bpmnElement="Flow_1x8x4em">
        <di:waypoint x="540" y="480" />
        <di:waypoint x="655" y="480" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1vc0d99_di" bpmnElement="Flow_1vc0d99">
        <di:waypoint x="525" y="160" />
        <di:waypoint x="480" y="160" />
        <di:waypoint x="480" y="440" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="495" y="173" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1hmiwsl_di" bpmnElement="Flow_1hmiwsl">
        <di:waypoint x="810" y="340" />
        <di:waypoint x="810" y="165" />
        <di:waypoint x="882" y="165" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1g7v2ai_di" bpmnElement="Flow_1g7v2ai">
        <di:waypoint x="705" y="480" />
        <di:waypoint x="810" y="480" />
        <di:waypoint x="810" y="420" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="742" y="493" width="15" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1t0ejbc_di" bpmnElement="Flow_1t0ejbc">
        <di:waypoint x="330" y="480" />
        <di:waypoint x="420" y="480" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1992bdp_di" bpmnElement="Flow_1992bdp">
        <di:waypoint x="250" y="-20" />
        <di:waypoint x="280" y="-20" />
        <di:waypoint x="280" y="440" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_01vvoai_di" bpmnElement="Flow_01vvoai">
        <di:waypoint x="550" y="135" />
        <di:waypoint x="550" y="-20" />
        <di:waypoint x="250" y="-20" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="561" y="118" width="23" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_05z3apo_di" bpmnElement="Flow_05z3apo">
        <di:waypoint x="1062" y="190" />
        <di:waypoint x="1062" y="260" />
        <di:waypoint x="110" y="260" />
        <di:waypoint x="110" y="0" />
        <di:waypoint x="150" y="0" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="1078" y="193" width="23" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0lqoezz_di" bpmnElement="Flow_0lqoezz">
        <di:waypoint x="8" y="-20" />
        <di:waypoint x="150" y="-20" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="41" y="-54" width="76" height="27" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1vqtafe_di" bpmnElement="Flow_1vqtafe">
        <di:waypoint x="2516" y="421" />
        <di:waypoint x="2600" y="421" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_0icw5c7_di" bpmnElement="Flow_0icw5c7">
        <di:waypoint x="2700" y="421" />
        <di:waypoint x="2755" y="421" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_1ru6ws5_di" bpmnElement="Flow_1ru6ws5">
        <di:waypoint x="2805" y="421" />
        <di:waypoint x="2980" y="421" />
        <di:waypoint x="2980" y="118" />
        <bpmndi:BPMNLabel>
          <dc:Bounds x="2871" y="396" width="23" height="14" />
        </bpmndi:BPMNLabel>
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNEdge id="Flow_16gnlzt_di" bpmnElement="Flow_16gnlzt">
        <di:waypoint x="2865" y="101" />
        <di:waypoint x="2962" y="100" />
      </bpmndi:BPMNEdge>
      <bpmndi:BPMNShape id="TextAnnotation_0cmctii_di" bpmnElement="TextAnnotation_0cmctii">
        <dc:Bounds x="220" y="-120" width="239.9788608806637" height="40.8423739629866" />
        <bpmndi:BPMNLabel />
      </bpmndi:BPMNShape>
      <bpmndi:BPMNEdge id="Association_14gerv3_di" bpmnElement="Association_14gerv3">
        <di:waypoint x="233" y="-60" />
        <di:waypoint x="248" y="-79" />
      </bpmndi:BPMNEdge>
    </bpmndi:BPMNPlane>
  </bpmndi:BPMNDiagram>
</bpmn:definitions>

<img width="8045" height="3900" alt="image" src="https://github.com/user-attachments/assets/7be7f560-0d91-4ce1-b331-0e1276d389a2" />
